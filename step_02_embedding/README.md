# 문서 임베딩 및 벡터 데이터베이스 생성

이 코드는 JSONL 형식의 문서를 읽어서 LangChain과 ChromaDB를 사용하여 임베딩하고 벡터 데이터베이스에 저장합니다.

## 설치 방법

필요한 패키지를 설치하려면 다음 명령어를 실행하세요:

```bash
pip install -r requirements.txt
```

## 사용 방법

1. `embedding.py` 파일을 실행합니다:

```bash
python embedding.py
```

2. 코드는 다음과 같은 작업을 수행합니다:
   - `../step_01_data_set/split_docs.jsonl` 파일에서 문서를 로드합니다.
   - 문서를 LangChain Document 객체로 변환합니다.
   - HuggingFace 임베딩 모델을 사용하여 문서를 임베딩합니다.
   - 임베딩된 문서를 ChromaDB 벡터 데이터베이스에 저장합니다.
   - 간단한 검색 테스트를 수행합니다.

## 커스터마이징

- 다른 임베딩 모델을 사용하려면 `create_embeddings()` 함수에서 `model_name` 매개변수를 변경하세요.
- 입력 파일 경로나 출력 디렉토리를 변경하려면 `main()` 함수에서 `input_file`과 `output_dir` 변수를 수정하세요.

## 참고 사항

- 이 코드는 HuggingFace의 `sentence-transformers/all-MiniLM-L6-v2` 모델을 사용합니다.
- 첫 실행 시 모델을 다운로드하므로 인터넷 연결이 필요합니다.
- 대용량 문서를 처리할 경우 충분한 메모리가 필요할 수 있습니다. 