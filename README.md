# SIYAQ: Sentiment Analysis and Linguistic Challenge Evaluation

SIYAQ compares two sentiment classification approaches and evaluates how they handle **contrastive language** and **negation**.

## 🔍 Models

- **TF-IDF + Logistic Regression** — a traditional word-based representation.
- **all-MiniLM-L6-v2 + Logistic Regression** — pretrained sentence embeddings with a Logistic Regression classifier.

## 📁 Repository Contents

- `SIYAQFINAL.ipynb` — complete implementation, evaluation, error analysis, and interactive prediction cell.
- `sentiment+labelled+sentences.zip` — dataset used in the project.

## 📊 Results

### Overall Test Set

| Model | Accuracy | Macro F1 |
|---|---:|---:|
| TF-IDF + Logistic Regression | 0.8202 | 0.8202 |
| MiniLM + Logistic Regression | **0.8674** | **0.8673** |

### Linguistic Challenge Subsets

| Model | Contrastive Accuracy | Contrastive Macro F1 | Negation Accuracy | Negation Macro F1 |
|---|---:|---:|---:|---:|
| TF-IDF + Logistic Regression | 0.6111 | 0.6000 | 0.7326 | 0.6434 |
| MiniLM + Logistic Regression | **0.7778** | **0.7662** | **0.8023** | **0.7574** |

**Key finding:** MiniLM achieved higher Accuracy and Macro F1 than TF-IDF across the overall test set and both linguistic challenge subsets.

**Subset sizes:** 18 verified contrastive examples and 86 negation examples. Only 4 examples contained both contrast and negation, so no separate overlap performance analysis was conducted.

## 🛠️ Environment and Requirements

- **Environment:** Jupyter Notebook
- **Python:** 3.10.18 (notebook environment)
- **Main libraries:** pandas, NumPy, scikit-learn, matplotlib, and sentence-transformers.
- The Setup section installs `sentence-transformers` and displays the installed package versions when the notebook is run.
- An internet connection is required the first time the pretrained `all-MiniLM-L6-v2` model is downloaded from Hugging Face.

## ▶️ How to Run

1. Clone or download this repository.
2. Keep `SIYAQFINAL.ipynb` and `sentiment+labelled+sentences.zip` in the same folder.
3. Open `SIYAQFINAL.ipynb` in Jupyter Notebook.
4. Run the notebook from top to bottom. The Setup section installs the required sentence-transformers package and extracts the dataset ZIP automatically.
5. To test a new review, edit the text in the **Try it** section and run that cell. It displays predictions from both models without retraining. Empty input is handled.

## 📚 Sources

- **Dataset:** [UCI Sentiment Labelled Sentences](https://archive.ics.uci.edu/dataset/331/sentiment+labelled+sentences)
- **Pretrained model:** [Sentence Transformers — all-MiniLM-L6-v2](https://huggingface.co/sentence-transformers/all-MiniLM-L6-v2)
- **Sentence Transformers documentation:** [sbert.net](https://www.sbert.net/)
- **Scikit-learn documentation:** [scikit-learn.org](https://scikit-learn.org/stable/)

