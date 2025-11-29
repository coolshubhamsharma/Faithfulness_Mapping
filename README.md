# BRSR Principle 6 — Faithfulness Mapping (Infosys)

This repository contains a Deep RAG (local) pipeline and deliverables for mapping SEBI BRSR Principle 6 (Environment)
to the Infosys BRSR report. It uses local embeddings (sentence-transformers) and FAISS for retrieval and a notebook
that generates drift scoring, Sankey and drift dashboard visuals, and a Word report.

## Files
- brsr_full_pipeline.ipynb — Jupyter notebook (end-to-end pipeline, local embeddings, FAISS, analysis)
- infosys_principle6_audit_with_sankey.docx — Final Word report (audit + embedded Sankey image)
- infosys_principle6_sankey_like.png — Evidence strength chart (Sankey-like)
- infosys_principle6_drift.png — Drift dashboard (color coded)
- requirements.txt — Python dependencies

## How to run (minimal)
1. Create virtualenv and install dependencies:
   ```bash
   python -m venv .venv
   source .venv/bin/activate   # Windows: .venv\Scripts\activate
   pip install -r requirements.txt
   ```

2. Open and run `brsr_full_pipeline.ipynb` in Jupyter or Colab. Place `sebi_brsr.pdf` and `company_brsr.pdf` in the working directory or update the paths in the notebook.

## Notes
- The notebook supports local embeddings with `sentence-transformers` and FAISS; no external API keys are required.
- The Word report and visuals were generated from the uploaded Infosys & SEBI PDFs and saved in the repo.
- For a more advanced LLM scoring step, you can plug in an LLM provider in the notebook (optional).

