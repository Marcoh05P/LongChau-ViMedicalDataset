# LongChau-ViMedical: A Vietnamese Medical Dataset for Classification

<p align="center">
  <img src="./docs/longchaupharmacy.png" alt="Long Chau Pharmacy logo" width="300">
</p>

<p align="left">
  <img alt="Dataset Version" src="https://img.shields.io/badge/dataset-v1.0.0-blue.svg">
  <img alt="Language" src="https://img.shields.io/badge/language-Vietnamese-brightgreen.svg">
  <img alt="Rows" src="https://img.shields.io/badge/rows-1500+-orange.svg">
  <img alt="License" src="https://img.shields.io/badge/license-CC%20BY--NC%204.0-green.svg">
  <img alt="GitHub Stars" src="https://img.shields.io/github/stars/Marcoh05P/LongChau-ViMedicalDataset?style=social">
  <img alt="GitHub Forks" src="https://img.shields.io/github/forks/Marcoh05P/LongChau-ViMedicalDataset?style=social">
</p>

---

## 📌 Introduction

The **LongChau-ViMedical Dataset** contains over 1,600 Vietnamese medical entries, including **disease categories**, **specific diseases** and their **symptoms**, crawled from [Long Chau Pharmacy](https://nhathuoclongchau.com.vn/).  

This dataset is designed to support **Natural Language Processing (NLP)** and other AI research in the Vietnamese medical domain. Key applications include:

- **Disease Classification:** Classify a disease based on a list of symptoms.  
- **Symptom-based Information Retrieval:** Retrieve relevant diseases given symptom queries.  
- **Medical Chatbots:** Power the knowledge base for symptom-checking bots.  
- **Fine-tuning LLMs:** Adapt large language models for Vietnamese medical knowledge.

---

## 📝 Dataset Description

- **Source:** [Long Chau Pharmacy](https://nhathuoclongchau.com.vn/)  
- **Language:** Vietnamese  
- **Total Rows:** 1,600+  
- **Format:** CSV (Comma-Separated Values)  

### Data Structure

| Column    | Description |
|-----------|-------------|
| `category` | Disease category/group |
| `disease`  | Disease name |
| `link`     | Source URL |
| `data`     | Symptoms / description |

---

## ⚙️ Usage

You can load the dataset easily using **pandas**:

```python
import pandas as pd

file_path = "data/raw/raw_medical_data.csv"

try:
    df = pd.read_csv(file_path)
    print(df.head())

    sample_category = df.iloc[0]['category']
    sample_disease = df.iloc[0]['disease']
    sample_symptoms = df.iloc[0]['data']

    print(f"\nCategory: {sample_category}")
    print(f"Disease: {sample_disease}")
    print(f"Symptoms: {sample_symptoms}")

except FileNotFoundError:
    print(f"Error: The file '{file_path}' was not found.")
except KeyError as e:
    print(f"Error: Missing column key: {e}")
except Exception as e:
    print(f"An error occurred: {e}")
```
## 🤝 Contributing

Contributions are welcome! You can help by:
* Cleaning and normalizing data
* Adding NLI pairs for NLP tasks
* Expanding categories or symptom coverage
* Reporting issues or errors in the dataset

Please follow standard commit message conventions and make pull requests against the main branch.

## ⚠️ License & Attribution

**License**: [CC BY-NC 4.0](https://creativecommons.org/licenses/by-nc/4.0/)
 – Non-commercial use only.

**Attribution**: This dataset is collected from Long Chau Pharmacy. All information belongs to the original source. Cite the dataset when using it in research or projects.

**Disclaimer**: This dataset is **not a substitute for professional medical advice, diagnosis or treatment**. Always seek advice from qualified healthcare providers.

---
*© 2025 Marcoh05P – LongChau-ViMedicalDataset – Ho Chi Minh City Open University*
