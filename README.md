# Phishing Email Detection Project

A data science project aimed at classifying emails as **Spam** or **Ham** (not spam) using machine learning techniques. This project processes email content, applies a trained **Naive Bayes classifier**, and evaluates its performance.

---

## Features
- **Preprocessing**: Text cleaning using tokenization, stopword removal, and lemmatization.
- **Model**: Multinomial Naive Bayes trained on TF-IDF features for robust text classification.
- **Evaluation**: Metrics like accuracy, precision, recall, and F1-score to assess model performance.
- **Visualization**: Includes WordClouds to show common spam/ham words.

---

## Installation

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/phishing-email-detector.git
   cd phishing-email-detector
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Download NLTK data:
   ```bash
   python
   >>> import nltk
   >>> nltk.download('stopwords')
   >>> nltk.download('wordnet')
   >>> exit()
   ```

4. Run the script:
   ```bash
   python phishing_email_detection.py
   ```

---

## How It Works

### Workflow:
1. **Data Preprocessing**:
   - Removes punctuation and special characters.
   - Converts text to lowercase.
   - Removes stopwords and applies lemmatization.

2. **Feature Extraction**:
   - Text is transformed into numerical features using TF-IDF vectorization.

3. **Model Training**:
   - A trained Multinomial Naive Bayes model predicts whether the email is Spam or Ham.

4. **Evaluation**:
   - Confusion matrix and classification report provide detailed performance metrics.

---

## File Structure

```
.
├── phishing_email_detection.py  # Main script for data processing and model training
├── phishing_model.pkl           # Trained Naive Bayes model
├── tfidf_vectorizer.pkl         # Trained TF-IDF vectorizer
├── requirements.txt             # Python dependencies
├── README.md                    # Project documentation
```

---

## Example Predictions
### Spam Email:
> **Input**:
> Congratulations! You've won a free ticket to the Bahamas. Click here to claim.
>
> **Prediction**:
> Spam

### Ham Email:
> **Input**:
> Hi, just checking in about the meeting tomorrow.
>
> **Prediction**:
> Ham

---

## Future Enhancements
- Add support for visualizing model performance over time.
- Experiment with deep learning models (e.g., LSTM or GRU).
- Enhance preprocessing to handle more nuanced cases like typos or slang.

---

## Contributing
Contributions are welcome! Please fork the repository and create a pull request with your changes.

---

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

## Acknowledgments
- **NLTK** for preprocessing tools.
- **Scikit-learn** for model building and evaluation.
- **WordCloud** for text visualizations.
