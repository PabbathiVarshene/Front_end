# 🌾 AgriAssist: AI-Based Crop Recommendation & Multilingual Farmer Chatbot

*AgriAssist* is a smart, AI-powered web application designed to assist farmers with crop recommendations and provide agricultural support through a multilingual chatbot. The system is optimized for low bandwidth usage and is fully functional without reliance on any external APIs.

---

## 🚀 Key Features

### ✅ 1. *AI-Powered Crop Recommendation*
- Predicts the most suitable crop based on soil and environmental features.
- Trained using a rich dataset with 14+ real-world features:
  - *Soil nutrients (N, P, K), temperature, humidity, pH, rainfall*
  - *Season, district, soil type, sunlight, water availability, fertilizers used*

### ✅ 2. *Multilingual Chatbot (English | Hindi | Telugu | +7 Languages)*
- Built using Hugging Face Transformers (distilbert-base-uncased-distilled-squad)
- Trained on a *custom dataset* across various categories:
  - *Greetings, Weather, Fertilizer Advice, Irrigation Tips, General Help, Fun, Motivation*
- Works entirely *offline* – no external API calls needed
- *Supports voice input and text-to-speech output*

### ✅ 3. *Web-Based UI with Bootstrap & JavaScript*
- Clean, mobile-responsive UI built with Bootstrap 5
- Interactive crop prediction form (AJAX-based fetch() requests to Flask backend)
- Chat interface with support for:
  - Language switching
  - Voice input (Web Speech API)
  - TTS output (SpeechSynthesis)

### ✅ 4. *Offline-First Architecture*
- No external APIs — all data, models, and logic are internal
- Minimal latency and low internet dependency

### ✅ 5. *Deployment-Ready*
- Can be deployed as:
  - A *web application* (Flask + HTML/JS/CSS)
  - A *mobile app* (via WebView or containerization)
- Ready for hosting on platforms like *Render, **Heroku, or **AWS EC2*

---

## 🧠 Technologies Used

| Component              | Tech Stack                        |
|------------------------|-----------------------------------|
| Backend                | Python, Flask, scikit-learn       |
| Chatbot                | HuggingFace Transformers, pandas  |
| ML Models              | Random Forest, LabelEncoder, Scaler |
| Frontend               | HTML5, CSS3, Bootstrap 5, JS      |
| Voice Features         | Web Speech API, SpeechSynthesis   |
| Model Persistence      | joblib (.pkl files)             |

---

 🏗 Project Structure

AgriAssist
│
├── app.py                      # Flask main backend
├── model/
│   └── crop_model.pkl          # Trained ML model
├── utils/
│   └── chatbot_logic.py        # Chatbot logic and pipeline
├── templates/
│   └── index.html              # Main frontend HTML
├── static/
│   ├── css/                    # Custom styles
│   ├── js/                     # JS for frontend logic (fetch, voice, TTS)
│
├── dataset/
│   ├── crop_dataset.csv        # For training model
│   └── farming_chatbot_big.csv# Chatbot question-answer dataset
└── README.md                   # Project readme
