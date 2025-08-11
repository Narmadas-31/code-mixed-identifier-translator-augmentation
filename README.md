# code-mixed-identifier-translator-augmentation
A robust system for identifying and translating code-mixed languages using synthetic data augmentation to improve model accuracy and generalization.
# Robust Code-Mixed Language Identification and Translation System with Synthetic Data Augmentation

##  Overview
This project implements a **robust end-to-end NLP pipeline** for:
1. **Identifying languages** in code-mixed Tamil-English text (including Romanized Tamil).
2. **Translating** code-mixed sentences into English.
3. Enhancing model **robustness** using **synthetic data augmentation**.

Key modules:
- **Custom preprocessing**: emoji removal, transliteration, token-level language detection.
- **Classification**: TF-IDF + Logistic Regression.
- **Data augmentation**: word-order perturbations to handle noisy social media text.
- **Neural machine translation**: Helsinki-NLP MarianMT multilingual model.
- **Evaluation**: BLEU score for translation quality.

---

##  Features
- **Language Identification** for mixed Tamil-English text.
- **Synthetic Data Augmentation** to improve model generalization.
- **Transliteration** for Romanized Tamil to Tamil script.
- **Translation to English** using open-source NMT models.
- **Evaluation Metrics** for both classification and translation.

---

##  Dataset
Uses the **DravidianCodeMix (2020)** dataset containing Tamil-English mixed sentences for tasks like:
- Sentiment analysis  
- Offensive language detection

>  Dataset is not included due to licensing. Instructions to download are given below.

---

##  Installation
```python
git clone https://github.com/Narmadas-31/code-mixed-identifier-translator-augmentation.git
cd code-mixed-identifier-translator-augmentation
pip install -r requirements.txt
```

---

##  Dataset Setup
1. Download the dataset from:  
   https://github.com/bharathichezhiyan/DravidianCodeMix-Dataset  
2. Extract it into the `data/` folder or update the dataset path in the code.

---

##  Usage

### **Option 1: Run the Notebook**
Open:
```python
[notebooks/main_pipeline.ipynb](notebooks/main_pipeline.ipynb)

```
and run all cells in order.

### **Option 2: Python Script**
If modularized into `src/`:
```python
python src/main.py
```
---

##  Results

### **Language Identification**
| Metric      | Value |
|-------------|-------|
| Accuracy    | 32%   |
| F1-Score    | 35%   |<macro avg>

### **Translation**
- BLEU Score: `3.04`

---

##  Example

**Input:**  
movie vara la level erika poguthu

**Preprocessed:**  
மூவி வர ல லெவல் எரிக போகுது

**Translation:**  
The movie is reaching the next level

---

##  Future Work
- Transformer-based classifiers (BERT, XLM-R) for identification.
- More augmentation methods: spelling errors, random insertions.
- Extension to Malayalam, Kannada code-mixed datasets.
- REST API for real-time processing.

---

##  License
MIT License — see [LICENSE](LICENSE) for details.

---

##  Acknowledgements
- [DravidianCodeMix Dataset](https://github.com/bharathichezhiyan/DravidianCodeMix-Dataset)  
- [Helsinki-NLP MarianMT models](https://huggingface.co/Helsinki-NLP)  
- [Indic Transliteration Library](https://pypi.org/project/indic-transliteration/)  

