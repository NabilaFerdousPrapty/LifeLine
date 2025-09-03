---

### Base Paper

**SAM-VQA: Visual Question Answering for Post-Disaster Damage Assessment**

- Published in IEEE Transactions on Geoscience and Remote Sensing (Q1 Journal).
- This paper proposes a supervised attention-based Visual Question Answering (VQA) model specifically designed to assess post-disaster damage using remote sensing aerial imagery.
- The model leverages the FloodNet-VQA dataset, which contains annotated images of flood-affected areas, enabling the system to answer disaster-related questions with high accuracy.
- The approach focuses on improving interpretability and effectiveness of VQA for disaster scenarios, aiding rapid and informed emergency response.
- Dataset & Code: https://github.com/Argho-UMBC/FloodNet-VQA

---

### Supporting Papers

1. **Better Safe Than Sorry? Overreaction Problem of Vision Language Models in Visual Emergency Recognition**

   - Addresses common issues faced by Vision-Language Models (VLMs) in emergency situations, particularly the overreaction problem where models can produce false or exaggerated responses.
   - Discusses methods to improve model robustness and contextual reasoning specific to safety-critical visual emergency recognition tasks.
   - This paper complements SAM-VQA by providing insights on improving reliability and reducing false positives in disaster VQA systems.
   - Link: https://arxiv.org/html/2505.15367v2

2. **Enhancing VQA for Flood Disaster Damage Assessment with Visual Contexts**

   - Proposes improvements to VQA models through the incorporation of richer visual context, leading to better zero-shot and few-shot learning capabilities in flood disaster scenarios.
   - Demonstrates that integrating stronger visual features and improved attention mechanisms significantly enhances question answering performance on flood-related damage assessment.
   - Offers techniques that can be adapted to extend and enhance the SAM-VQA framework.
   - Link: https://arxiv.org/pdf/2312.13848.pdf

3. **Analysis of Multimodal Social Media Data Utilizing ViT Base 16 and GPT-2 for Disaster Response**
   - Explores multimodal (image and text) social media data classification using Vision Transformer (ViT Base 16) and generative language modeling (GPT-2) for disaster response.
   - Provides practical methodology to extract real-time, ground-level information from social media that complements aerial remote sensing data.
   - Useful for integrating social media insights into a comprehensive disaster preparedness system combining remote sensing and on-ground data.
   - Paper: https://doi.org/10.1007/s13369-025-10314-7
   - Dataset: CrisisMMD — https://crisisnlp.qcri.org/crisismmd/
   - Code: https://github.com/Arundarasi89/Multi-modal-codes

---

These papers collectively provide a strong foundation for building a Vision-Language Model-based Visual Question Answering system that integrates aerial remote sensing and social media data to enhance disaster preparedness and response capabilities.
