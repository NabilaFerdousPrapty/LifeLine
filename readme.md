

# Multimodal Disaster Classification using CLIP 

This repository contains the official implementation of a high-precision multimodal classifier for disaster response. By leveraging **Weight-Decomposed Low-Rank Adaptation (DoRA)** on a **CLIP** backbone, this project surpasses traditional full fine-tuning benchmarks (89%) to achieve **>90% accuracy** on the CrisisMMD dataset while training only **~2.5%** of the parameters.

---

## 🚀 Key Features

* **State-of-the-Art Fine-Tuning:** Implements **DoRA**, which decouples magnitude and direction updates to match full fine-tuning performance with massive efficiency.
* **Multimodal Alignment:** Utilizes a custom **Projection Alignment** layer and **Trainable LayerNorms** to calibrate CLIP's generic embeddings for noisy, disaster-specific social media data.
* **Complex Classification:** Supports three critical humanitarian tasks:
1. **Task 1:** Informative vs. Non-informative (Binary)
2. **Task 2:** Humanitarian Categories (8-class: Infrastructure, Affected People, etc.)
3. **Task 3:** Damage Severity Assessment (Severe, Mild, None)


* **Optimized Training:** Includes Cosine Annealing with Warmup and Label Smoothing to prevent overfitting and ensure stability.

---

## 📊 Performance Comparison

| Method | Trainable Params | Val Accuracy (Binary) | GPU VRAM |
| --- | --- | --- | --- |
| Full Fine-Tuning | 100% (150M+) | 89.00% | >24 GB |
| Standard LoRA () | ~3.7% | 87.53% | <8 GB |
| **Proposed DoRA + LN Adaptation** | **~2.52% (3.9M)** | **90.42%** | **<8 GB** |

---

## 🛠️ Installation

```bash
# Clone the repository
git clone https://github.com/your-username/multimodal-disaster-dora.git
cd multimodal-disaster-dora

# Install dependencies
pip install torch torchvision transformers peft pillow pandas tqdm scikit-learn

```

---

## 📂 Dataset

This project uses **CrisisMMD**, a multimodal Twitter dataset consisting of ~18,000 image-text pairs from seven major 2017 disasters.

**Structure:**

* `data/CrisisMMD/task_informative_text_img_train.tsv`
* `data/CrisisMMD/task_humanitarian_text_img_train.tsv`

---

## 🧠 Model Architecture

The core of the model is a **CLIP (ViT-B/32)** backbone. We inject low-rank adapters into the `q_proj`, `v_proj`, and `MLP` blocks of both the vision and text encoders.

**Why DoRA?**
Standard LoRA only scales weights. **DoRA** decomposes weight updates () into magnitude () and direction ():



This allowed us to break the "89% ceiling" by giving the adapters the same directional freedom as full fine-tuning.

---

## 📈 Training Progress

The model benefits from a **25% Warmup Phase** to calibrate the unfrozen LayerNorms before aggressive learning begins.

---

## 📝 Usage

```python
from model import MultimodalDisasterClassifier
from peft import PeftModel

# Load the base model
base_model = MultimodalDisasterClassifier(model_id="openai/clip-vit-base-patch32", num_classes=8)

# Load the best DoRA weights
model = PeftModel.from_pretrained(base_model, "checkpoints/best_90plus_stable")
model.to("cuda")

# Run inference
outputs = model(input_ids, attention_mask, pixel_values)

```

---

## 🎓 Citation

If you use this code or our findings in your research, please cite:

```bibtex


```

---

**Would you like me to help you create a specific "How to contribute" or "License" section to complete this file?**
