# Design Notes — Final Project: RAG + TTS Question-Answering System

**Goal:** Have students build a complete, document-grounded QA system end-to-end — retrieval, generation, and speech output — using only free/open models, runnable on Google Colab (with optional GPU).

**Pipeline specified:**
1. Document ingestion (paste or `.txt` upload)
2. Chunking with overlap (suggested: `chunk_size=650`, `overlap=120`)
3. Embedding each chunk (suggested model: `all-MiniLM-L6-v2`)
4. Vector indexing with FAISS
5. Query embedding + top-k retrieval (`top_k=3–5`)
6. Prompt assembly restricting the LLM to answer only from retrieved context
7. Generation (suggested model: `Qwen2.5-1.5B-Instruct`)
8. Text-to-speech playback (`gTTS`)
9. Simple chat UI (`Gradio`)

**Constraints imposed on students:**
- No paid APIs — free/open-source models only
- Must explicitly state "not in document" if the answer isn't supported by the source text
- Should surface which retrieved chunks were used as sources (grounding/explainability)
- Evaluated against a 5,000–9,000 word English source document

**Bonus extension:** Detect Persian-language source documents, translate to English for indexing/retrieval, translate user questions to English at query time, generate in English, then translate the answer back to Persian — while keeping the answer grounded in the source document.

**Why this design:** Forces students to reason about retrieval quality, prompt grounding, and hallucination control, not just "call an LLM API" — while the free-model constraint keeps cost and infra accessible for a classroom setting.
