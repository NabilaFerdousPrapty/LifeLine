

# Multimodal Disaster Classification using CLIP 

This repository contains the official implementation of a high-precision multimodal classifier for disaster response. By leveraging **Weight-Decomposed Low-Rank Adaptation (DoRA)** on a **CLIP** backbone, this project surpasses traditional full fine-tuning benchmarks (89%) to achieve **>90% accuracy** on the CrisisMMD dataset while training only **~2.5%** of the parameters.

---

Social media generates massive multimodal data during disasters, yet automated triage remains challenged by semantic ambiguity and computational latency. This paper presents Crisis-CLIP, a resource-efficient framework for real-time crisis classification. Utilizing a Dynamic Gated Fusion mechanism, the model aligns visual and textual features to perform simultaneous relevance filtering, categorization, and severity assessment. Validated on the CrisisMMD benchmark, the system achieves 89.27% accuracy and a critical 98% recall for infrastructure damage. Unlike heavy generative models, our unified encoder architecture is optimized for edge deployment. Benchmarking on a consumer-grade NVIDIA RTX 3050 Laptop GPU confirms a sustained throughput of 491.47 posts per second, validating the framework's capability to process high-velocity crisis data in real-time without expensive cloud infrastructure.
