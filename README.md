# 📚 Literature‑Map

Transform any BibTeX library into an **interactive, shareable 2‑D map** of your research field—powered by modern sentence embeddings, t‑SNE/UMAP, and Plotly.

---

## ✨ Key Features

| Stage              | What it does                                                                                             | Tech                                            |
| ------------------ | -------------------------------------------------------------------------------------------------------- | ----------------------------------------------- |
| Parse & Clean      | Convert `.bib` → tidy `pandas` DataFrame; strip LaTeX, deduplicate, back‑fill missing DOIs from CrossRef | `bibtexparser`, `pandas`                        |
| Embed              | Turn *title + abstract* into dense vectors via **Google Gemini** or **Sentence‑Transformers**            | `google‑generativeai` • `sentence‑transformers` |
| Reduce             | PCA (50 →) t‑SNE/UMAP (→ 2 D) for visual layout                                                          | `scikit‑learn`, `umap‑learn`                    |
| Visualise          | Interactive Plotly scatter—hover for metadata, zoom, filter                                              | `plotly`                                        |

---

## 🚀 Quick Start

```bash
# 1. Clone & install
pip install -r requirements.txt

# 2. Drop your BibTeX file into ./data/
cp ~/Downloads/library.bib data/

# 3. Run the notebook      # OR run the CLI pipeline
jupyter lab literature_map.ipynb

# 4. Open the result
open literature_map.html
```

> **⚠️ API keys** – If you use Gemini embeddings, set `export GEMINI_API_KEY=…` before running. Otherwise the pipeline falls back to a local Sentence‑Transformer.

---

## 🙌 Contributing

All feedback & bug reports welcome via GitHub Issues.

---

## 📄 License

Distributed under the **MIT License**. See `LICENSE` for details.

---

## 📜 Citation

If you use *Literature‑Map* in academic work, please cite:

```text
@misc{literaturemap2025,
  title   = {Literature‑Map: Interactive 2‑D visualisation of academic corpora},
  author  = {Your Name et al.},
  year    = {2025},
  howpublished = {GitHub repository},
  url     = {https://github.com/yourname/literature-map}
}
```

Happy mapping 🗺✨

