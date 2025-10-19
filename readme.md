# 📌 Lifeline

**Learning-based Interactive Framework for Emergency and Lifesaving INsight Extraction**

**Lifeline** is a research framework that adapts **Multimodal** to answer natural language questions about **remote sensing imagery** for disaster preparedness and response.

When every second counts, Lifeline provides **interactive, explainable, and trustworthy AI insights** from satellite/UAV data.

---

## 🚀 Features

- Vision-Language Models (VLMs) for **Visual Question Answering (VQA)**
- Disaster-related tasks: preparedness (risk, vulnerability) & response (damage, accessibility)
- **Explainability**: attention maps & heatmaps
- Support for **yes/no, counting, and descriptive answers**
- Lightweight **LoRA/QLoRA fine-tuning** for domain adaptation
- Modular dataset loading (FloodNet-VQA, xBD, RSIVQA, etc.)

---

## 📂 Repository Structure

```bash
Lifeline/
│── README.md                # Project overview (this file)
│── requirements.txt         # Python dependencies
│── setup.py                 # Installation script (optional)
│── .gitignore
│
├── data/                    # Datasets (scripts & links, not raw data)
│   ├── raw/                 # Original datasets
│   ├── processed/           # Preprocessed Q&A and image tiles
│   └── README.md            # Dataset sources & setup guide
│
├── notebooks/               # Jupyter notebooks for experiments
│   ├── 01_dataset_prep.ipynb
│   ├── 02_baseline_vqa.ipynb
│   ├── 03_lora_finetune.ipynb
│   ├── 04_evaluation.ipynb
│   └── 05_visualizations.ipynb
│
├── src/                     # Source code
│   ├── config/              # Config files
│   ├── data_loader.py       # Data preprocessing & loaders
│   ├── model/               # Model definitions
│   │   ├── baseline_vqa.py
│   │   ├── vlm_adapter.py
│   │   └── attention_utils.py
│   ├── training/            # Training scripts
│   │   ├── train_baseline.py
│   │   ├── train_lora.py
│   │   └── utils.py
│   ├── inference/           # Inference & explainability
│   │   ├── predict.py
│   │   ├── explain.py
│   │   └── demo_ui.py
│   └── evaluation/          # Metrics & evaluation
│       ├── vqa_metrics.py
│       └── attention_eval.py
│
├── models/                  # Pretrained & fine-tuned weights
│   ├── baseline/
│   └── lifeline_lora/
│
├── results/                 # Logs, predictions, visualizations
│   ├── attention_maps/
│   ├── predictions.json
│   └── evaluation_report.csv
│
└── docs/                    # Documentation
    ├── proposal.pdf
    ├── architecture.png
    └── gantt_plan.png
```

---

## ⚙️ Installation

```bash
git clone https://github.com/your-username/Lifeline.git
cd Lifeline
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows

pip install -r requirements.txt
```

---

## ▶️ Usage

### Preprocess Dataset

```bash
python src/data_loader.py --dataset floodnet --tile-size 512
```

### Train Baseline VQA

```bash
python src/training/train_baseline.py --epochs 20
```

### Fine-tune with LoRA

```bash
python src/training/train_lora.py --model blip2 --dataset floodnet
```

### Run Inference

```bash
python src/inference/predict.py --image sample.png --question "How many flooded buildings?"
```

### Visualize Attention

```bash
python src/inference/explain.py --image sample.png --question "Is the road accessible?"
```

---

## 📊 Datasets

- **FloodNet-VQA** (UAV images, flood Q\&A)
- **xBD** (satellite pre/post building damage)
- **RSIVQA / VQA-RS** (remote sensing VQA benchmarks)

_(See `data/README.md` for setup instructions)_

---

## 📅 Roadmap (Thesis Plan)

- [x] Dataset preprocessing pipeline
- [x] Baseline VQA implementation
- [ ] LoRA fine-tuning for remote sensing VQA
- [ ] Evaluation & attention visualization
- [ ] Prototype demo UI
- [ ] Thesis writing & final report

---

## 🙌 Acknowledgements

- [FloodNet-VQA](https://github.com/BinaLab/FloodNet)
- [xBD](https://xview2.org/)
- [BLIP-2](https://github.com/salesforce/LAVIS), [LLaVA](https://llava-vl.github.io/)

---

✨ **Lifeline: Learning-based Interactive Framework for Emergency and Lifesaving INsight Extraction.**
