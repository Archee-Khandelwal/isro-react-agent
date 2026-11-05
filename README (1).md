# ISRO Missions ReAct Agent (Assignment 2)

A ReAct-style agent built with the Gemini API in Google Colab. The model **reasons** about the question,
**acts** by calling a `search_documents` tool, reads the result, and loops until it can answer.

Document set: 4 short documents on Indian space missions: Chandrayaan-3, Mangalyaan, Aditya-L1 and PSLV-C37.

## Changes made to the starter `agent_loop_demo.ipynb`
- Filled `DOCUMENTS` with 4 documents (5 sentences each).
- Fixed `search_recipes` -> `search_documents` (was a NameError in two places).
- Replaced the invalid model name `"claude"` with `gemini-3.5-flash-lite`.
- Passed the system instruction into `GenerateContentConfig` (the starter never sent it to the model).
- Rewrote the system instruction for the space-missions domain.
- Added stop-word filtering to the search tool so words like "the" don't match every document.
- Added 3 domain questions, keeping the out-of-scope and general-knowledge test questions.

## Run
Open the notebook in Colab, add `GOOGLE_API_KEY` under **Secrets** (key icon), then **Runtime -> Run all**.

Author: Bhavayraj Singhal
