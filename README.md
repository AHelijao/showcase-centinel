# Centinel — showcase

**Portfolio:** [ahelijao.github.io](https://ahelijao.github.io/) · Chapter II

> Sanitized public view. Source and document corpora stay private.

## What it is

An **offline cyber knowledge base**: RAG over compliance and methodology PDFs (ISO, DORA, GDPR/RGPD, NIST, OWASP, PTES), queried in natural language via a **local LLM** (Ollama). Methodology questions get **phased** answers (prep → execution → evidence).

## Problem

Security pros need to interrogate dense frameworks without uploading proprietary or sensitive docs to a cloud LLM — and without dumping unstructured wall-of-text answers.

## What this shows

- Local embeddings + vector store (offline-first)
- Separation of *compliance rules* vs *methodology steps* in retrieval
- Structured responses for auditor / pentester workflows

## Stack

`Python` · `ChromaDB` · `Ollama` · PDF ingest · RAG

## Status

Personal / research tooling. No corpus, no model weights, no runtime config in this repo.

---

*Helijao Andriamandranto — software & cybersecurity*
