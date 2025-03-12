# Tips & Tricks

A collection of quick tips to help you get the most out of Roo Code.

- Drag Roo Code to the [Secondary Sidebar](https://code.visualstudio.com/api/ux-guidelines/sidebars#secondary-sidebar) so you can see the Explorer, Search, Source Control, etc.
- Once you have Roo Code in a separate sidebar from the file explorer, you can drag files from the explorer into the chat window (and even multiple at once). Just make sure to hold down the shift key after you start dragging the files.
- If you're not using [MCP](/advanced-usage/mcp), turn it off in the <Codicon name="notebook" /> Prompts tab to significantly cut down the size of the system prompt.
- To keep your [custom modes](/advanced-usage/custom-modes) on track, limit the types of files that they're allowed to edit.
- If you hit the dreaded `input length and max tokens exceed context limit` error, you can recover by deleting a message, rolling back to a previous checkpoint, or switching over to a model with a long context window like Gemini for a message.
- In general, be thoughtful about your `Max Tokens` setting for thinking models. Every token you allocate to that takes away from space available to store conversation history. Consider only using high `Max Tokens` / `Max Thinking Tokens` settings with modes like Architect and Debug, and keeping Code mode at 16k max tokens or less.
- If there's a real world job posting for something you want a custom mode to do, try asking Code mode to `Create a custom mode based on the job posting at @[url]`
- If you want to really accelerate, check out multiple copies of your repository and run Roo Code on all of them in parallel (using git to resolve any conflicts, same as with human devs).
- Add your own tips by clicking "Edit this page" below!
