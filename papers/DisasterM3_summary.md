---

## Thesis Proposal

### Title

Development and Evaluation of a Vision-Language Visual Question Answering System for Disaster Preparedness and Response

### Introduction

Rapid and accurate disaster response depends on timely assessment of damage and needs. Visual Question Answering (VQA) systems, combining image analysis and natural language processing, offer interactive solutions for extracting actionable information from disaster imagery. This thesis focuses on developing and evaluating a supervised attention-based VQA system (SAM-VQA) using remote sensing and aerial images for disaster damage assessment. Additionally, it explores integration of multimodal social media data analysis to detect urgent help-seeking content, thereby broadening the scope and relevance of the system.

### Problem Statement

Current disaster damage assessment methods are often slow, manual, or lack interactivity. While SAM-VQA provides state-of-the-art VQA functionality on aerial images, it does not address the growing need to analyze social media multimodal data for immediate, ground-level situational awareness. This research aims to enhance disaster preparedness tools by combining aerial image VQA with social media multimodal classification, providing rapid, rich, and multifaceted insights to responders.

### Objectives

- Implement and fine-tune the SAM-VQA supervised attention framework on the FloodNet-VQA dataset.
- Develop a multimodal classification module inspired by transformer-based social media data analysis (ViT + GPT-2 ensemble) to detect critical help requests from social media posts.
- Integrate both modules into a unified disaster preparedness chatbot interface offering image-based question answering and social media content filtering.
- Evaluate system performance quantitatively (accuracy, precision, recall) and qualitatively (usefulness in simulated disaster scenarios).

### Methodology

- Use SAM-VQA codebase and FloodNet-VQA data for supervised attention VQA model training and testing.
- Implement multimodal social media classifier using ViT Base 16 for images and GPT-2 for text on CrisisMMD or similar datasets.
- Fuse outputs via ensemble learning and design the chatbot interface for user interaction.
- Conduct extensive experiments, hyperparameter tuning, and usability testing.

### Expected Contributions

- Enhanced disaster response tool combining remote sensing VQA and social media multimodal analysis.
- Novel insights on integrating supervised attention VQA with transformer-based multimodal classifiers.
- Prototype chatbot system deployable as a decision support tool for emergency responders.

---

## Future Plan

1. **Extended Dataset Integration:**  
   Incorporate other disaster datasets beyond FloodNet-VQA and CrisisMMD to improve model generalizability across different disaster types and regions.

2. **Explainability and Visualization:**  
   Develop explainability modules to visualize attention maps for VQA predictions and provide interpretable insights, increasing trust and user adoption.

3. **Real-Time Deployment and Optimization:**  
   Explore model pruning, quantization, and lightweight transformer versions (e.g., TinyVQA, MobileViT, DistilGPT) to enable real-time applications on edge devices such as drones or smartphones.

4. **Multilingual and Cross-Platform Social Media Analysis:**  
   Adapt social media module to support multiple languages and platforms (Instagram, Facebook) to widen applicability in diverse disaster regions.

5. **User-Centered Interface Enhancements:**  
   Design and test user-friendly, voice-enabled chatbot interfaces for responders in the field, facilitating hands-free operation under stressful conditions.

6. **Collaborative Response System:**  
   Integrate the chatbot into emergency management workflows with automatic alert generation, resource coordination, and update sharing among stakeholders.
