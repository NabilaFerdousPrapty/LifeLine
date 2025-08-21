# 📂 GitHub Repo Structure for Thesis (Disaster Preparedness GPT + VLM)

```
📁 Disaster-Preparedness-GPT
│── README.md                  # Project overview (what your thesis is about)
│
├── 📂 notes/                   # Notes & learning materials
│   ├── llm_basics.md           # Notes on LLM, GPT, Transformers
│   ├── rag_basics.md           # Notes on RAG concepts
│   ├── vlm_basics.md           # Notes on BLIP-2, LLaVA, etc.
│   ├── datasets.md             # Notes on CrisisMMD, DisasterM3, Kaggle datasets
│   └── literature_review.md    # Your summaries of papers (MARSHA, DisasterM3, etc.)
│
├── 📂 papers/                  # Reference papers (PDFs or summaries)
│   ├── MARSHA_summary.md
│   ├── DisasterM3_summary.md
│   ├── VLM_Q1paper_summary.md
│   └── related_work.md
│
├── 📂 proposal/                # Proposal drafts
│   ├── full_proposal.md        # 2–3 page version (the one we made)
│   ├── short_pitch.md          # 1-page pitch version
│   └── timeline.md             # Weekly roadmap
│
├── 📂 datasets/                # Links, exploration, samples
│   ├── dataset_links.md        # Kaggle, Hugging Face, CrisisMMD URLs
│   ├── preprocessing_notes.md
│   └── sample_data/            # Store tiny samples (not full dataset)
│
├── 📂 experiments/             # Later when you test models
│   ├── rag_demo.ipynb          # Jupyter notebook for text RAG demo
│   ├── vlm_demo.ipynb          # BLIP-2 / LLaVA test notebook
│   └── multimodal_pipeline.md  # Notes on combining text + vision
│
└── 📂 thesis_draft/            # Writing drafts
    ├── chapter1_intro.md
    ├── chapter2_lit_review.md
    ├── chapter3_methodology.md
    ├── chapter4_results.md
    └── chapter5_conclusion.md
```

---

```
LifeLine-Disaster-Preparedness-Assistant/
│
├── 📂 data/                         # Datasets
│   ├── text/                        # Disaster preparedness docs, PDFs
│   ├── images/                      # Flood images (from Kaggle, CrisisMMD, etc.)
│   └── processed/                   # Cleaned/annotated data for training/testing
│
├── 📂 notebooks/                    # Jupyter notebooks for experiments
│   ├── 01_rag_basics.ipynb          # RAG pipeline with disaster text
│   ├── 02_vlm_basics.ipynb          # Testing VLMs on flood images
│   ├── 03_integration.ipynb         # Combining RAG + VLM
│   └── 04_chatbot_demo.ipynb        # Prototype chatbot
│
├── 📂 src/                          # Source code
│   ├── rag_pipeline.py              # Retrieval-Augmented Generation pipeline
│   ├── vlm_module.py                # Vision-Language Model integration
│   ├── chatbot.py                   # Main chatbot logic (merges RAG + VLM)
│   ├── evaluation.py                # Evaluation metrics
│   └── utils.py                     # Helper functions
│
├── 📂 configs/                      # Configuration files
│   ├── model_config.yaml            # VLM + LLM model settings
│   └── database_config.yaml         # Vector DB / embeddings setup
│
├── 📂 results/                      # Results and logs
│   ├── eval_reports/                # Evaluation reports (accuracy, relevance, etc.)
│   ├── examples/                    # Example Q&A outputs
│   └── images/                      # Sample chatbot screenshots
│
├── 📂 thesis/                       # Writing materials
│   ├── references.bib               # BibTeX references
│   ├── outline.md                   # Thesis outline
│   ├── drafts/                      # Draft chapters
│   └── figures/                     # Diagrams for thesis
│
├── requirements.txt                 # Python dependencies
├── README.md                        # Project description
└── LICENSE                          # License file
```

# 📝 What to Save as Notes (Markdown files)

### **1. Learning Notes**

- `llm_basics.md` → Transformers, GPT, Fine-tuning, Prompting.
- `rag_basics.md` → What is RAG, why it reduces hallucination.
- `vlm_basics.md` → How BLIP-2, LLaVA work.
- `datasets.md` → Dataset sources + basic exploration.

### **2. Literature Review**

- Each paper you read → summary in **5 bullet points**.
- Example (MARSHA):

  - Goal: Multi-agent RAG for hazard adaptation.
  - Strength: Novel architecture for adaptation.
  - Limitation: No multimodal support.
  - Dataset: Not specified (text-based).
  - My gap: Add VLM support.

### **3. Proposal**

- Full proposal (2–3 pages) → `proposal/full_proposal.md`.
- 1-page pitch version → `proposal/short_pitch.md`.
- Roadmap timeline → `proposal/timeline.md`.

### **4. Thesis Draft**

- Write each chapter separately in `thesis_draft/`.
- Easier to merge later into Word/PDF.

---
