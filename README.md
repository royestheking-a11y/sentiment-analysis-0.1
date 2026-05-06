# Bangla Sentiment Analysis Using Machine Learning

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)](https://www.python.org/downloads/release/python-380/)

## 📝 Overview
This project aims to classify the sentiment of Bangla social media comments (Facebook, YouTube, Daraz) into three categories: **Positive**, **Negative**, and **Neutral**. We leverage traditional Machine Learning (SVM, Naive Bayes) and Deep Learning (LSTM, BiLSTM) architectures to achieve high accuracy on morphologically rich Bangla text.

## 📁 Project Structure
```text
bangla-sentiment-analysis/
│
├── data/
│   ├── raw_comments.csv      # Unprocessed data (10,000+ entries)
│   └── annotated_data.csv    # Manually labeled dataset with confidence scores
│
├── lexicon/
│   ├── emoji_lexicon.csv     # 300+ emojis with sentiment scores
│   ├── slang_dict.csv        # 600+ Bangla slangs and informal terms
│   └── stopwords.txt         # 300+ Bangla stopwords
│
├── models/                   # Saved model weights and binaries
│   ├── svm_model.pkl
│   └── lstm_model.h5
│
├── results/
│   ├── test_predictions.csv  # Sample predictions on test set
│   ├── results.json          # Metrics (Accuracy, Precision, Recall, F1)
│   └── training_history.csv  # Loss and Accuracy over epochs
│
├── notebooks/
│   ├── preprocessing.ipynb   # Text cleaning, tokenization, and normalization
│   └── training.ipynb        # Model training and evaluation
│
├── README.md
└── requirements.txt
```

## 🚀 Getting Started

### Prerequisites
Ensure you have Python 3.8+ installed.

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/mizanur-rahman/bangla-sentiment-analysis.git
   cd bangla-sentiment-analysis
   ```
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

## 📊 Dataset
The dataset consists of **10,000+ comments** collected from various social media platforms.
- **Labels:** Positive, Negative, Neutral.
- **Features:** Original text, Platform, Date, Annotator votes, Confidence level.

## 🛠 Methodology
1. **Preprocessing:** 
   - Emoji handling (using emoji lexicon).
   - Slang normalization (using slang dictionary).
   - Stopword removal.
   - Stemming/Lemmatization.
2. **Feature Extraction:** 
   - TF-IDF for ML models.
   - Word Embeddings (Word2Vec/FastText) for Deep Learning models.
3. **Models:** 
   - Support Vector Machine (SVM)
   - Multinomial Naive Bayes
   - Long Short-Term Memory (LSTM)
   - Bidirectional LSTM (BiLSTM)

## 📈 Results
The BiLSTM model achieved the highest performance:
| Model | Accuracy | F1-Score |
| :--- | :--- | :--- |
| **BiLSTM** | **90%** | **0.88** |
| LSTM | 88% | 0.86 |
| SVM | 82% | 0.79 |
| Naive Bayes | 75% | 0.73 |

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a Pull Request.

## 👤 Author
**Mizanur Rahman**
- [GitHub](https://github.com/aurangzeb-sunny)
- [LinkedIn](https://www.linkedin.com/in/aurangzebsunny/)
- [Google Scholar](https://scholar.google.com/citations?user=YOUR_ID) <!-- Replace with your actual Google Scholar ID -->

## 📚 Citation
If you find this project useful in your research, please cite it:

```bibtex
@software{Rahman_Sentiment_Analysis_2026,
  author = {Rahman, Mizanur},
  month = {5},
  title = {{Sentiment Analysis of Social Media Comments using BiLSTM}},
  url = {https://github.com/royestheking-a11y/sentiment-analysis-0.1},
  version = {0.1.0},
  year = {2026}
}
```

## 📄 License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
