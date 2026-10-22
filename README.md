# Centinel — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter II  
**Private source:** not linked

> Docs-only public view. No PDF corpus, no vector DB dumps, no runtime config.

## Elevator

**Offline cyber knowledge base** — RAG over compliance & methodology documents, queried in natural language through a **local LLM**. Built for auditors / security engineers who cannot ship docs to a public cloud model.

## Need

| Pain | Response |
|------|----------|
| Dense frameworks (ISO, DORA, GDPR/RGPD, NIST, OWASP, PTES) | Ingest PDFs → local vector index |
| Unstructured LLM answers | **Methodology-driven** replies in execution phases |
| Cloud leakage risk | Embeddings + LLM **offline** (Ollama-class) |

## Architecture (sanitized)

```text
PDF corpus (local)
       │
       ▼
┌──────────────────┐     ┌─────────────────┐
│  Ingest / chunk  │────▶│  Vector store   │
│  (PDF pipeline)  │     │  (e.g. Chroma)  │
└──────────────────┘     └────────┬────────┘
                                  │ retrieve
                                  ▼
                         ┌─────────────────┐
                         │  Local LLM      │
                         │  phased answer  │
                         └─────────────────┘
```

**Retrieval idea:** tag content as *rules/compliance* vs *steps/methodology*, then bias answers when the question is a “how to”.

## What this demonstrates

- Production-shaped **RAG**, not a toy chat over one file
- Security posture: **data never leaves the machine** by design
- UX for practitioners (structured phases, not vibes)

## Stack

`Python` · `ChromaDB` · LlamaIndex-style orchestration · `Ollama` embeddings/LLM · `pypdf`

## Explicitly not in this repo

Source, `requirements` lock with secrets, indexed storage, private PDFs.

---

← back to [portfolio](https://ahelijao.github.io/) · Helijao Andriamandranto
