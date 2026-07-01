# RAG Retrieval Strategy Evaluation

This project evaluates and compares different retrieval strategies for Retrieval-Augmented Generation (RAG) systems. It uses the [CRAG (Corrective Retrieval Augmented Generation)](https://huggingface.co/datasets/Quivr/CRAG) dataset to benchmark the performance of keyword-based search against semantic vector search and hybrid fusion methods.

## Features
- **BM25 Retrieval:** Traditional keyword-based search using the `bm25s` library.
- **Semantic Search:** Dense retrieval using `Sentence-Transformers` (`BAAI/bge-base-en-v1.5`).
- **Reciprocal Rank Fusion (RRF):** A hybrid approach that combines BM25 and Semantic Search rankings to improve retrieval accuracy.
- **Automated Evaluation:** Calculates Top-5 Hit Rate across multiple query categories (e.g., Simple, Multi-hop, Comparison).

## Methodology
The evaluation compares three retrieval methods across categorized query sets from the CRAG dataset. Each method is evaluated on its ability to retrieve the ground-truth document within the top 5 results.



## Prerequisites
To run this notebook, you will need an environment with the following libraries:
- `bm25s`
- `sentence-transformers`
- `datasets`
- `transformers`

Install dependencies using:
```bash
pip install bm25s sentence-transformers datasets transformers
