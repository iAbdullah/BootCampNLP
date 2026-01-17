# 📂 CV Organizer: Unsupervised Topic Modeling with LDA 🤖

![Python](https://img.shields.io/badge/python-3670A0?style=for-the-badge&logo=python&logoColor=ffdd54)
![Scikit-Learn](https://img.shields.io/badge/scikit--learn-%23F7931E.svg?style=for-the-badge&logo=scikit-learn&logoColor=white)
![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?style=for-the-badge&logo=numpy&logoColor=white)
![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?style=for-the-badge&logo=pandas&logoColor=white)
![JSON](https://img.shields.io/badge/json-5E5E5E?style=for-the-badge&logo=json&logoColor=white)

> **"Organize the chaos of unlabeled resumes automatically."** > This project uses **Latent Dirichlet Allocation (LDA)** to discover hidden topics in CVs and sort them into folders without manual labeling.

---

## 🚀 Concept: Proving General Utility of Embeddings
This project is designed to meet the requirements of exploring NLP techniques beyond simple text classification:
* **Another Dataset**: Instead of using standard song/video playlists, we applied Recommender System concepts to **Professional Resumes**.
* **Tokens are not just Words**: In this model, tokens represent **Technical Skills and Professional IDs**, proving that mathematical embeddings are useful in diverse domains like HR and Recruitment.



---

## 🌟 Key Features
* **Unsupervised Categorization** 🧠: Automatically groups resumes into themes like *AI, Web Dev, or HR*.
* **Multilingual NLP** 🌍: Optimized for cleaning and processing both **Arabic and English** text.
* **Flexible Data Loader** 📄: Handles various JSON structures (Lists and Dictionaries).
* **Folder-Based Organization** 📁: Automatically creates a directory structure based on dominant topics.

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

## 📊 How to Use
1. **Prepare Data**: Place your JSON CV files in the `datasets/` folder.
2. **Run the Notebook**: Open `08_topic_modeling_ex.ipynb` and run all cells.
3. **Check Results**: View the `output/organized_cvs/` folder to see your resumes automatically sorted.

---

## 💡 Why LDA for CVs?
Latent Dirichlet Allocation is a generative statistical model that proves:
* **Efficiency**: No need to manually read thousands of CVs to categorize them.
* **Accuracy**: It finds recurring patterns (tokens) that define a specific career path
