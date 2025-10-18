# Sentiment Analysis on YouTube Educational Video Comments

## Overview

This project focuses on **sentiment analysis of YouTube comments** for educational videos using state-of-the-art NLP models. The goal is to understand the viewers’ feedback, detect patterns in opinions, and quantify the overall sentiment trends. The analysis leverages transformer-based models like **DeBERTa v3, ALBERT, DistilBERT, RoBERTa**, combined with a **Multi-Layer Perceptron (MLP)** for classification and evaluation.

---

## Features

* Collects and preprocesses YouTube comments from educational videos.
* Performs **sentiment classification** (positive, neutral, negative) using multiple transformer-based NLP models.
* Compares model performances in terms of accuracy, F1-score, and other metrics.
* Visualizes the results with **charts and graphs** to highlight sentiment trends.
* Provides a clear analysis of patterns and viewer engagement through comments.

---

## Models Used

| Model          | Description                                                                    |
| -------------- | ------------------------------------------------------------------------------ |
| **DeBERTa v3** | Decoding-enhanced BERT with disentangled attention; powerful for NLP tasks.    |
| **ALBERT**     | A lightweight BERT variant optimized for efficiency and performance.           |
| **DistilBERT** | A smaller, faster version of BERT; good for real-time applications.            |
| **RoBERTa**    | Robustly optimized BERT; great for high-accuracy NLP classification.           |
| **MLP**        | Multi-Layer Perceptron used on top of embeddings for sentiment classification. |

---

## Dataset

* Comments were collected from **educational YouTube videos** using YouTube Data API v3.
* Dataset includes:

  * Comment text
  * Video ID
  * Author info (optional)
  * Timestamp
* Data is preprocessed: cleaned, lowercased, tokenized, and encoded for transformer inputs.

---

## Installation

1. Clone the repository:

```bash
git clone https://github.com/your-username/YouTubeSentimentAnalysis.git
cd YouTubeSentimentAnalysis
```

2. Create a virtual environment:

```bash
python -m venv env
source env/bin/activate  # For Linux/Mac
env\Scripts\activate     # For Windows
```

3. Install required packages:

```bash
pip install -r requirements.txt
```

---

## Usage

1. **Preprocess the dataset**:

```bash
python preprocessing.py --input comments.csv --output processed_comments.csv
```

2. **Train models**:

```bash
python train.py --model deberta_v3 --data processed_comments.csv
python train.py --model albert --data processed_comments.csv
python train.py --model roberta --data processed_comments.csv
```

3. **Evaluate results**:

```bash
python evaluate.py --model deberta_v3 --data processed_comments.csv
```

4. **Visualize sentiment trends**:

```bash
python visualize.py --data results.csv
```

---

## Results & Observations

* All models achieved high accuracy for classifying positive and negative sentiments.
* **DeBERTa v3** consistently performed the best due to its disentangled attention mechanism.
* MLP on top of embeddings helped improve classification performance in some models.
* Viewer comments were generally **positive**, showing high engagement for educational content.
* Some challenges were observed in classifying **neutral comments**, highlighting the subtlety in sentiment expression.

---

## Future Work

* Expand dataset to include **different languages**.
* Integrate **topic modeling** to combine sentiment with content analysis.
* Use **ensemble methods** to combine transformer outputs for improved performance.
* Deploy as a **real-time sentiment analysis dashboard** for YouTube channels.

---

## Requirements

* Python 3.8+
* Libraries: `transformers`, `torch`, `scikit-learn`, `pandas`, `matplotlib`, `numpy`
* YouTube Data API key (for comment extraction)

---

## License

This project is licensed under the MIT License – see the [LICENSE](LICENSE) file for details.


Veux‑tu que je fasse ça aussi ?
