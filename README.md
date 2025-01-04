# SPAM-CLASSIFY


# Email Spam Classification

## Overview

This project classifies emails as **spam** or **ham** (not spam) using a machine learning approach. It employs **Logistic Regression** and **TF-IDF vectorization** for feature extraction and training. The dataset is preprocessed to remove null values and encoded for the classification task.

## Features

- Cleans and preprocesses text data.
- Extracts features using **TF-IDF Vectorizer**.
- Trains a **Logistic Regression** model for classification.
- Evaluates model performance using **accuracy** on training data.

## Prerequisites

Ensure the following are installed in your Python environment:

- Python 3.7 or higher
- `numpy`
- `pandas`
- `scikit-learn`

Install dependencies using:
```bash
pip install numpy pandas scikit-learn
```

## Dataset

The dataset used contains two columns:
- **Category**: Label for each email (`ham` or `spam`).
- **Message**: The text content of the email.

Example:
| Category | Message                                      |
|----------|----------------------------------------------|
| ham      | Go until jurong point, crazy..              |
| spam     | Free entry in 2 a wkly comp to win FA Cup...|

You can replace `mail data.csv` with any dataset following this format.

## Project Structure

```
email-spam-classification/
│
├── mail_data.csv          # Dataset file
├── main.py                # Main script for training and evaluation
├── README.md              # Project documentation
└── requirements.txt       # Dependencies
```

## Usage

1. **Clone the repository**:
    ```bash
    git clone https://github.com/your-repo/email-spam-classification.git
    cd email-spam-classification
    ```

2. **Place your dataset**:
   Ensure your dataset (e.g., `mail data.csv`) is in the project directory.

3. **Run the code**:
   Execute the notebook or main script to train the model and evaluate its accuracy:
   ```bash
   python main.py
   ```

4. **Results**:
   The output includes:
   - Feature extraction details.
   - Training accuracy.

## Code Explanation

### 1. Data Preprocessing
- Load data from a CSV file using `pandas`.
- Replace null values with an empty string.
- Encode `ham` as `1` and `spam` as `0`.

### 2. Feature Extraction
- Use **TF-IDF Vectorizer** to transform email content into numerical feature vectors.
- Stop words are removed, and case normalization is applied.

### 3. Model Training
- The **Logistic Regression** model is trained on the TF-IDF transformed training data.

### 4. Evaluation
- Predictions are made on training data, and accuracy is computed using `accuracy_score`.





## Future Enhancements

- Add cross-validation for better performance evaluation.
- Test and evaluate on unseen test data.
- Extend support for additional languages and email formats.


