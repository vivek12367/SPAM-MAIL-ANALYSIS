# Phishing Email Detection 

This project processes email content, applies a trained **Naive Bayes classifier**, and provides real-time predictions via a user-friendly web interface.

---

## Features
- **Preprocessing**: Text cleaning using tokenization, stopword removal, and lemmatization.
- **Model**: Multinomial Naive Bayes trained on TF-IDF features for robust text classification.
- **Visualization**: Includes WordClouds to show common spam/ham words.
- **Scalable Deployment**: Can be deployed on Heroku, Streamlit Cloud, or AWS.

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

4. Run the application:
   - For Flask:
     ```bash
     python app.py
     ```
   - For Streamlit:
     ```bash
     streamlit run app.py
     ```

5. Access the app:
   - Flask: Visit [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.
   - Streamlit: The URL will be displayed in the terminal.

---

## How It Works

### Workflow:
1. **Data Preprocessing**:
   - Removes punctuation and special characters.
   - Converts text to lowercase.
   - Removes stopwords and applies lemmatization.

2. **Feature Extraction**:
   - Text is transformed into numerical features using TF-IDF vectorization.

3. **Prediction**:
   - A trained Multinomial Naive Bayes model predicts whether the email is Spam or Ham.

4. **Interactive Output**:
   - Displays results immediately after user input.

---

## File Structure

```
.
├── app.py                 # Main Flask/Streamlit application file
├── phishing_model.pkl     # Trained Naive Bayes model
├── tfidf_vectorizer.pkl   # Trained TF-IDF vectorizer
├── templates/             # HTML templates (for Flask)
│   └── index.html
├── static/                # Static assets (e.g., CSS, JS)
├── requirements.txt       # Python dependencies
├── README.md              # Project documentation
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

## Deployment

### Local Deployment
Run the application locally using Flask or Streamlit as described in the **Installation** section.

### Cloud Deployment
1. **Heroku**:
   - Install Heroku CLI: [https://devcenter.heroku.com/articles/heroku-cli](https://devcenter.heroku.com/articles/heroku-cli)
   - Deploy using the following commands:
     ```bash
     heroku login
     git init
     heroku create
     git add .
     git commit -m "Initial commit"
     git push heroku master
     ```

2. **Streamlit Cloud**:
   - Deploy directly from your repository to [Streamlit Cloud](https://streamlit.io/).

---

## Future Enhancements
- Add support for file uploads (e.g., `.csv` or `.txt` for bulk predictions).
- Implement a deep learning model (e.g., LSTM or GRU) for improved accuracy.
- Enhance the frontend with more interactive visualizations.
- Integrate with an email client for real-time phishing detection.

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
