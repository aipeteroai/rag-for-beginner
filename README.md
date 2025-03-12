# Roo - RAG 시스템 구현 프로젝트

이 프로젝트는 Retrieval-Augmented Generation (RAG) 시스템을 Python으로 구현하는 입문자를 위한 튜토리얼입니다. Roo Code의 공식 문서를 기반으로 RAG 시스템을 단계별로 구현합니다.

## 프로젝트 구조

프로젝트는 다음과 같은 단계별 디렉토리로 구성되어 있습니다:

- **step_00_data_download**: GitHub에서 데이터셋 다운로드
- **step_01_data_set**: 원본 데이터 준비 및 JSONL 포맷으로 변환
- **step_02_embedding**: 데이터 임베딩 및 벡터 DB 구성
- **step_03_RAG**: 리트리버 구성 및 RAG 시스템 완성
- **chroma_db**: 벡터 데이터베이스 저장소

## 환경 설정

### 1. Python 버전

이 프로젝트는 Python 3.10 이상이 필요합니다.

### 2. 의존성 관리 (uv)

이 프로젝트는 `uv`를 사용하여 의존성을 관리합니다. `uv`는 빠르고 안정적인 Python 패키지 관리자입니다.

#### uv 설치

```bash
pip install uv
```

#### 의존성 설치

```bash
uv pip install -e .
```

#### 의존성 동기화

프로젝트의 의존성을 동기화하려면 다음 명령어를 실행하세요:

```bash
uv pip sync
```

### 3. 환경 변수 설정

1. `.env.sample` 파일을 `.env`로 복사합니다:

```bash
cp .env.sample .env
```

2. `.env` 파일을 열고 OpenAI API 키를 입력합니다:

```
OPENAI_API_KEY=your_openai_api_key
```

**중요**: 실제 OpenAI API 키로 `your_openai_api_key`를 교체해야 합니다. API 키가 없다면 [OpenAI 웹사이트](https://platform.openai.com/)에서 발급받을 수 있습니다.

## 실행 방법

각 단계별 디렉토리에 있는 Jupyter 노트북을 순서대로 실행하세요:

1. `step_00_data_download/download.ipynb`: 데이터 다운로드
2. `step_01_data_set/데이터조사_가공.ipynb`: 데이터 가공
3. `step_02_embedding/embedding.ipynb`: 임베딩 생성
4. `step_03_RAG/RAG.ipynb`: RAG 시스템 구현 및 테스트

## 주요 기능

- GitHub에서 문서 데이터셋 다운로드
- LangChain을 활용한 문서 처리 및 메타데이터 생성
- 문서 임베딩 및 ChromaDB 벡터 데이터베이스 구성
- BM25와 벡터 유사도 검색을 결합한 앙상블 리트리버 구현
- OpenAI API를 활용한 RAG 시스템 구현

## 의존성

- chromadb: 벡터 데이터베이스
- langchain: LLM 애플리케이션 프레임워크
- langchain-openai: OpenAI 통합
- pandas: 데이터 처리
- rank-bm25: BM25 검색 알고리즘
- 기타 의존성은 `pyproject.toml` 파일 참조

## 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다. 자세한 내용은 [LICENSE](LICENSE) 파일을 참조하세요.
