# Detecting Mental Health Conditions from Social Media Posts Using Deep Learning

### Project Overview

This project explores multi-modal deep learning models to detect mental health conditions from Reddit posts. We used BiLSTM, tuned BiLSTM, TextCNN, and DistilBERT to identify indicators of mental distress. The best-performing model (DistilBERT) achieved 98.01% accuracy and 0.998 AUC, highlighting the effectiveness of transformer-based models in this domain.

### Objective

* Develop a tool for early mental health detection using NLP and deep learning.
* Compare various deep learning architectures in terms of performance and efficiency.
* Integrate text content and metadata features for robust classification.

### Dataset

* **Source:** Reddit Mental Health Dataset (via Zenodo)
* **Size:** 90,718 posts (53,868 positive, 36,850 control)
* **Labels:** Binary (1 = mental health-related, 0 = control)

### Preprocessing

* Text cleaning, tokenization, padding/truncation
* Train-test split (80/20 stratified)
* Sequence length: 300 (for BiLSTM and CNN) or 128 (for DistilBERT)

### Models Implemented

1. **BiLSTM (Baseline)**

   * Accuracy: 97.27%
   * Loss: 0.1037
2. **Tuned BiLSTM**

   * Accuracy: 97.6%
   * AUC: 0.996
3. **DistilBERT (Transformer-based)**

   * Accuracy: 98.01%
   * AUC: 0.9982
4. **TextCNN**

   * Accuracy: 97.15%
   * AUC: 0.9959

### Evaluation Metrics

* Accuracy
* F1-Score
* ROC-AUC
* Confusion Matrix

### Key Insights

* Transformer-based models outperform traditional RNNs and CNNs.
* Hyperparameter tuning improves performance marginally for BiLSTM.
* CNN models converge faster and require less computational power.
* All models achieved strong performance, making them viable for real-world deployment.

### Tools & Libraries

* Python, TensorFlow, Keras, HuggingFace Transformers, scikit-learn
* Google Colab environment

### Conclusion

DistilBERT is the most effective model for mental health text classification in our experiments. Its high accuracy and nearly perfect AUC make it ideal for use in clinical or digital health applications. Lighter models like BiLSTM or CNN offer efficiency advantages for deployment in resource-constrained settings.

### Future Work

* Integrate multimodal signals (e.g., time, user metadata)
* Use domain-specific pretraining or ensemble methods
* Extend to multi-class classification for finer-grained mental health conditions

---

© 2025 Northeastern University | Mental Health NLP Project
