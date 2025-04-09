# 📰 Fake News & Media Bias Detection System

An automated Python-based system that scrapes news articles from major sources via RSS feeds and uses machine learning to detect fake news and media bias.

## 🚀 Features

- Collects real-world news articles hourly from RSS feeds (BBC, CNN, Al Jazeera, etc.)
- Extracts article text using `newspaper3k`
- Detects:
  - **Fake news** using a pre-trained BERT model
  - **Bias** in language using another fine-tuned BERT model
  - **Sentiment** via `TextBlob`
- Stores processed data in:
  - CSV file (as a backup)
  - MongoDB (for structured querying)
- Logs everything in real time
- Extracts keywords using `CountVectorizer`

## 🛠️ Tech Stack

- Python
- Transformers (BERT)
- PyTorch
- Newspaper3k
- MongoDB (via `pymongo`)
- TextBlob, Scikit-learn
- RSS/XML Parsing
- AsyncIO

## 📁 Project Structure

```
📦project-root/
├── News_fake_bias_detection.py   # Main runner script
├── requirements.txt              # Dependencies
├── processed_articles.json       # Tracks already processed URLs
├── news_articles.csv             # CSV backup of articles
├── data/                         # Log and output storage
├── bert_fake_1000_model/        # Folder with fake news model and tokenizer
├── bert_bias_model/             # Folder with bias model and tokenizer
└── README.md
```

## 🧪 How to Run

```bash
pip install -r requirements.txt
python News_fake_bias_detection.py
```

Make sure your fake/bias models are located in the paths specified in the script:
- `bert_fake_model`
- `bert_bias_model`

## ⚙️ MongoDB Setup

Update the MongoDB credentials in the script:

```python
MONGODB_USERNAME = "your_username"
MONGODB_PASSWORD = "your_password"
```

## 📄 License

This project is licensed under the MIT License.
