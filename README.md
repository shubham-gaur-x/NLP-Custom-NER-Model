
# Sentiment Analysis and Custom Named Entity Recognition (NER) Project

## Overview
This project explores two key areas of Natural Language Processing (NLP):  
1. **Sentiment Analysis**: Predicting customer sentiment (positive or negative) based on restaurant reviews.  
2. **Custom Named Entity Recognition (NER)**: Extracting specific entities (e.g., products, people, prices) from customer reviews.  

The project leverages machine learning and NLP techniques to provide insights into customer behavior and improve service quality.

---

## Features
### Sentiment Analysis
- **Dataset**: 1,000 restaurant reviews labeled as positive (1) or negative (0).  
- **Models**:  
  - Simple RNN: Achieved 67% accuracy.  
  - LSTM: Achieved 74% accuracy, with better generalization and lower validation loss.  
- **Performance Metrics**: Accuracy, Precision, Recall, and F1 Score.  
- **Visualizations**: Word cloud showing the most frequently mentioned words in reviews.

### Custom NER
- **Dataset**: Annotated customer reviews with labeled entities.  
- **Entity Classes**:  
  - PERSON: Staff or customer names.  
  - LOC: Locations such as restaurant names or cities.  
  - PRODUCT: Food items or menu-specific mentions.  
  - MONEY: Prices, deals, or promotions.  
  - TIME: References to waiting times or event times.  
- **Insights**: Extracted key entities from reviews to identify product mentions, service feedback, pricing sensitivity, and time-related issues.

---

## Project Structure
```
Sentiment_NER_Project/
├── data/
│   ├── reviews.csv          # Sentiment analysis dataset
│   ├── ner_annotations.json # Annotated data for NER model
├── models/
│   ├── sentiment_rnn.py     # Simple RNN implementation
│   ├── sentiment_lstm.py    # LSTM implementation
│   ├── ner_model.py         # Custom NER model
├── notebooks/
│   ├── sentiment_analysis.ipynb # Sentiment analysis development
│   ├── ner_analysis.ipynb       # NER development and insights
├── scripts/
│   ├── train_sentiment.py    # Training script for sentiment models
│   ├── train_ner.py          # Training script for NER model
├── requirements.txt          # Dependencies
└── README.md                 # Project documentation
```

---

## Setup and Installation

### Prerequisites
- Python 3.8 or higher.
- Install dependencies using pip:  
  ```bash
  pip install -r requirements.txt
  ```

### Run the Project
1. **Train the Sentiment Analysis Models**:  
   ```bash
   python scripts/train_sentiment.py
   ```
2. **Train the NER Model**:  
   ```bash
   python scripts/train_ner.py
   ```
3. **Interactive Analysis**:  
   Open the notebooks in the `notebooks/` directory to explore detailed steps and visualizations.

---

## Key Insights
1. **Sentiment Analysis**:  
   - LSTM outperformed Simple RNN in all evaluation metrics, achieving a higher F1 score of 0.75.  
   - Enhanced models with hyperparameter tuning improved performance slightly but highlighted the complexity of the dataset.

2. **Custom NER**:  
   - Extracted actionable insights from customer reviews, such as frequently mentioned products, service quality feedback, and pricing sensitivity.  
   - High precision and recall for PRODUCT and MONEY entities provided valuable insights for businesses.

---

## Future Work
- Enhance sentiment analysis models with larger datasets and additional preprocessing techniques.  
- Expand NER entity classes to capture more nuanced feedback.  
- Experiment with transformer-based models like BERT for both sentiment analysis and NER tasks.

---

## License
This project is for academic purposes and is not licensed for commercial use.

## Acknowledgments
- Dataset sources and tools used:  
  - Restaurant reviews dataset for sentiment analysis.  
  - SpaCy for custom NER model development.  
  - Matplotlib and Seaborn for visualizations.

---
