

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

# 📝 What to Save as Notes (Markdown files)

### **1. Learning Notes**

* `llm_basics.md` → Transformers, GPT, Fine-tuning, Prompting.
* `rag_basics.md` → What is RAG, why it reduces hallucination.
* `vlm_basics.md` → How BLIP-2, LLaVA work.
* `datasets.md` → Dataset sources + basic exploration.

### **2. Literature Review**

* Each paper you read → summary in **5 bullet points**.
* Example (MARSHA):

  * Goal: Multi-agent RAG for hazard adaptation.
  * Strength: Novel architecture for adaptation.
  * Limitation: No multimodal support.
  * Dataset: Not specified (text-based).
  * My gap: Add VLM support.

### **3. Proposal**

* Full proposal (2–3 pages) → `proposal/full_proposal.md`.
* 1-page pitch version → `proposal/short_pitch.md`.
* Roadmap timeline → `proposal/timeline.md`.

### **4. Thesis Draft**

* Write each chapter separately in `thesis_draft/`.
* Easier to merge later into Word/PDF.

---
