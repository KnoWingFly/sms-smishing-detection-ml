# SMS-Smishing-Detection-ML

## 1. Project Title

**XAI-Enhanced Smishing Detection: A Comparative Study of Ensemble and Deep Learning**

This project focuses on identifying and classifying "Smishing" (SMS Phishing) attacks using a combination of traditional Machine Learning ensemble methods and modern Deep Learning architectures, supplemented by Explainable AI (XAI) principles for better model interpretability.

---

## 2. Code / Dataset Description

The repository contains a comprehensive pipeline for smishing detection. It integrates multiple datasets to create a robust training environment. The codebase includes:

- **Feature Engineering**: Automated detection of embedded URLs, Email addresses, and Phone numbers within SMS content.
- **NLP Pipeline**: Full text preprocessing including normalization, tokenization, stopword filtering, and lemmatization.
- **Hybrid Modeling**: Implementation of both Ensemble models (XGBoost, Random Forest, Stacking) and Deep Learning (Bidirectional LSTM) to compare performance.
- **Evaluation**: Rigorous testing using F1-Score, Precision, and Recall to ensure reliability in detecting malicious messages.

---

## 3. Dataset Information

This project utilizes a combination of three datasets to ensure diversity and robustness:

1.  **SMS PHISHING DATASET FOR MACHINE LEARNING AND PATTERN RECOGNITION**
    - **Content**: A collection of SMS messages labeled for phishing and pattern recognition research.
    - **Link**: [Mendeley Data](https://data.mendeley.com/datasets/f45bkkt8pr/1)

2.  **A Balanced Dataset for Spam and Smishing Detection using Large Language Models (LLMs)**
    - **Content**: A modern, balanced dataset specifically designed for training LLMs and deep learning models on spam and smishing.
    - **Link**: [Mendeley Data](https://data.mendeley.com/datasets/vmg875v4xs/1)

3.  **Smishing_Dataset (Combined Labeled Dataset)**
    - **Content**: A large-scale combined dataset containing over 80,000 labeled SMS entries.
    - **Link**: [GitHub Repository](https://github.com/shaghayegh-hp/Smishing_Dataset/blob/main/Combined-Labeled-Dataset.csv)

---

## 4. Code Description

| File                      | Description                                                                                               |
| :------------------------ | :-------------------------------------------------------------------------------------------------------- |
| `smising-detection.ipynb` | Main Jupyter Notebook containing the full end-to-end pipeline (EDA, Preprocessing, Training, Evaluation). |
| `dataset/`                | Directory intended for storing the CSV files downloaded from the sources above.                           |
| `CITATION.cff`            | Citation metadata for the project.                                                                        |

---

## 5. Usage Instructions

Follow these steps to reproduce the results:

1.  **Clone the Repository**:
    ```bash
    git clone https://github.com/KnoWingFly/sms-smishing-detection-ml
    cd sms-smishing-detection-ml
    ```
2.  **Install Dependencies**:
    Ensure you have Python installed, then run:
    ```bash
    pip install pandas numpy matplotlib nltk scikit-learn xgboost tensorflow imbalanced-learn
    ```
3.  **Prepare Datasets**:
    - Download the datasets from the links in Section 3.
    - Place the CSV files in the `dataset/` directory.
4.  **Run the Notebook**:
    - Open `smising-detection.ipynb` in Jupyter Lab or Google Colab.
    - Execute the cells sequentially to perform data integration, cleaning, and model training.
5.  **Evaluate Models**:
    - Review the classification reports and confusion matrices at the end of the notebook.

---

## 6. Requirements

- **Language**: Python 3.8+
- **Libraries**:
  - `pandas`, `numpy`: Data manipulation
  - `nltk`: Natural Language Processing
  - `scikit-learn`: Machine Learning algorithms and evaluation
  - `xgboost`: Gradient Boosting Ensemble
  - `tensorflow`/`keras`: Deep Learning (LSTM/Bi-LSTM)
  - `matplotlib`, `seaborn`: Data visualization
  - `imblearn`: Handling class imbalance (SMOTE)

---

## 7. Methodology for Code Usage

The project follows a structured data science methodology:

1.  **Data Integration**: Merging multiple CSV sources and standardizing labels (Ham, Spam, Smishing).
2.  **Feature Extraction**: Using Regular Expressions (Regex) to extract structural features (URLs, Emails, Phones).
3.  **Text Preprocessing**:
    - Case Folding & Cleaning (Removing special characters).
    - Tokenization (NLTK).
    - Stopword Removal (Customized to keep high-impact words like "urgent", "win").
    - Lemmatization (WordNet).
4.  **Handling Imbalance**: Applying **SMOTE** to balance the smishing vs. ham classes.
5.  **Model Training**:
    - **Ensemble**: Random Forest, XGBoost, Stacking Classifier.
    - **Deep Learning**: Bidirectional LSTM with Embedding layers.
6.  **XAI Integration**: Interpreting model decisions through feature importance analysis.

---

## 8. Citation

Not applicable.

---

## 9. License & Contribution Guidelines

Not applicable.

---

## 10. Code Repository or DOI

- **Repository**: [https://github.com/KnoWingFly/sms-smishing-detection-ml](https://github.com/KnoWingFly/sms-smishing-detection-ml)
- **DOI**: [![DOI](https://zenodo.org/badge/1215004888.svg)](https://doi.org/10.5281/zenodo.19651117)
