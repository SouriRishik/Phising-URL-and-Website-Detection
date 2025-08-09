# 🛡️ Phishing URLs and Websites detection using Machine Learning

A machine learning-based web application to detect phishing websites using features extracted from URLs. This project uses a trained CatBoost model for classification and provides a user-friendly interface via Flask.

---

## 📌 Table of Contents

- [Features](#-features)
- [Dataset](#-dataset)
- [Installation](#-installation)
- [Usage](#-usage)
- [Project Structure](#-project-structure)
- [Model](#-model)
- [Demo](#-demo)
- [License](#-license)

---

## 🚀 Features

- Extracts lexical and host-based features from URLs
- Utilizes a pre-trained CatBoost classifier
- Simple and intuitive web UI for URL classification
- Supports real-time prediction
- Deployed with Flask and ready for platforms like Heroku

---

## 📂 Dataset

The model is trained on a dataset (`phishing.csv`) containing labeled URLs:
- `0`: Legitimate URL  
- `1`: Phishing URL  

The dataset includes features like:
- Presence of `@` symbol
- Length of URL
- Use of `https`, IP address, etc.

---

## 🔧 Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/SouriRishik/Phising-URL-and-Website-Detection.git
   cd Phising-URL-and-Website-Detection
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the application**
   ```bash
   python app.py
   ```

---

## 💻 Usage

1. Start the app with `python app.py`
2. Navigate to `http://localhost:5000` in your browser
3. Enter any URL to check if it's phishing or legitimate

---

## 🧠 Model

- The model is trained using **CatBoost**, optimized for performance and interpretability.
- The feature extraction logic is found in `feature.py`
- The trained model is stored in the `pickle/` directory and loaded during runtime

---

## 🗂️ Project Structure

```
Phishing-URL-Detection/
├── app.py                   # Main Flask application
├── feature.py               # URL feature extractor
├── Phishing URL Detection.ipynb  # Training & evaluation notebook
├── phishing.csv             # Training dataset
├── requirements.txt         # Project dependencies
├── pickle/                  # Contains the serialized ML model
├── static/                  # Static assets (CSS/images)
├── templates/               # HTML templates
├── Procfile                 # For deployment (e.g., Heroku)
└── README.md
```

