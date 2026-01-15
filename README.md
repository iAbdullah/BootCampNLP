# 📂 CV Organizer: Unsupervised Topic Modeling with LDA 🤖

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![JSON](https://img.shields.io/badge/json-5E5E5E?style=for-the-badge&logo=json&logoColor=white)

> **"Organize the chaos of unlabeled resumes automatically."** > This project uses **Latent Dirichlet Allocation (LDA)** to discover hidden topics in CVs and sort them into folders without manual labeling.

---

## 🌟 Key Features
* **Unsupervised Categorization** 🧠: Automatically groups resumes into themes like *AI, Web Dev, or HR*.
* **Multilingual NLP** 🌍: Optimized for cleaning and processing both **Arabic and English** text.
* **Flexible Data Loader** 📄: Robustly handles various JSON structures (Lists and Dictionaries).
* **Folder-Based Organization** 📁: Automatically creates a directory structure and moves files based on their dominant topic.

---

## 🛠️ Technical Pipeline

| Stage | Process | Description |
| :--- | :--- | :--- |
| **1. Ingestion** | `glob` & `json` | Scans for `.json` files and extracts raw text regardless of structure. |
| **2. Cleaning** | `Regex` | Removes emails, URLs, and symbols while preserving language characters. |
| **3. Vectorization** | `CountVectorizer` | Converts cleaned text into a Document-Term Matrix (Bag of Words). |
| **4. Modeling** | `LDA` | Learns the distribution of words across a set number of topics. |
| **5. Sorting** | `shutil` | Automatically moves CVs into folders based on the model's prediction. |



---

## 📁 Repository Structure
```text
├── 08_topic_modeling_ex.ipynb   # 📓 Main Python Notebook
├── datasets/                    # 📥 Input: Raw JSON CV files
└── output/                      # 📤 Output: Categorized Results
    └── organized_cvs/
        ├── Topic_1/             # 💻 e.g., Software Engineering
        ├── Topic_2/             # 📊 e.g., Data Science
        └── Topic_3/             # 🛠️ e.g., Operations
