**Sample Lightweight Demo Experiment on A-RAG**
(Read it here - https://arxiv.org/pdf/2602.03442)
Modern RAG (Retrieval-Augmented Generation) systems help LLMs answer questions by fetching documents. But most current RAG systems are rigid:
Either they retrieve once and dump everything into the model
Or they follow a fixed workflow (step 1 → step 2 → step 3)
The key issue:
 👉 The model itself doesn’t decide how to search.
The paper introduces A-RAG (Agentic RAG):
👉 Treat the language model as an active agent that controls retrieval
A-RAG gives the model a hierarchical toolkit:
1. Keyword search (coarse)
Like Google search
Good for broad exploration
2. Semantic search (medium)
Finds meaning-related passages
Good for refining results
3. Chunk read (fine-grained)
Read a specific document chunk
Good for deep inspection
👉 This creates a multi-scale retrieval system
 —from broad → precise.
hink of it like this:
Question → model decides:
   → keyword search
   → refine with semantic search
   → read chunks
   → maybe search again
→ final answer
So instead of a pipeline, it’s a feedback loop.
