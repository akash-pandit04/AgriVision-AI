# AgriVision AI

A full-stack intelligent agriculture platform combining computer vision, machine learning, and real-time weather data to help farmers make smarter decisions for healthier crops and a greener future.

# Problem Statement

In modern agriculture, farmers face unpredictable weather, crop diseases, and inefficient resource usage. There is no efficient method to:
- Quickly identify and diagnose crop diseases before they spread
- Determine the best-fit crops based on complex soil conditions, NPK values, and climate
- Make optimal irrigation decisions based on real-time soil moisture and weather data

This application addresses this problem by providing an AI-powered platform that analyzes agricultural data and offers actionable insights, helping farmers improve yield and reduce resource waste.

# Features
- Farmer Can upload leaf images for instant AI disease detection with confidence scores
- Farmer Can receive crop recommendations based on soil, NPK, season, and climate
- Farmer Can access smart irrigation decisions based on soil moisture & weather
- Farmer Can interact with an AI Farmer Assistant (chatbot) in English, Hindi, and Gujarati
- Farmer Can view real-time weather intelligence and a sustainability score

# Admin / System Manager
- Can view overall platform usage and API health
- Can monitor active AI model endpoints and inference times
- Can view analysis report for all disease detection requests
- Can export system logs to a file

## How to Run

```bash
# Terminal 1: Start Backend (FastAPI)
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload --port 8000

# Terminal 2: Start Frontend (React)
cd frontend
npm install
npm run dev
```

Open **http://localhost:5173** in your browser.

## Sample Run

```
====================================
      AgriVision AI Server Startup
====================================
INFO:     Will watch for changes in these directories: ['/backend']
INFO:     Uvicorn running on http://127.0.0.1:8000 (Press CTRL+C to quit)
INFO:     Started reloader process [12345] using StatReload
INFO:     Started server process [12347]
INFO:     Waiting for application startup.
INFO:     AI Models Loaded:
          - Disease Detection (PyTorch)
          - Crop Recommendation (RandomForest)
INFO:     Application startup complete.
====================================

--- API Request Log ---
[POST] /api/disease-detect -> 200 OK (Confidence: 94.2% - Tomato Early Blight)
[POST] /api/crop-recommend -> 200 OK (Recommended: Wheat)
[GET]  /api/weather        -> 200 OK (Temp: 28°C, Humidity: 65%)
```

---

## 🧠 AI Models

| Module | Description |
|---|---|
| 🦠 **Disease Detection** | Upload a leaf image → AI detects disease with confidence score |
| 🌾 **Crop Recommendation** | Get best-fit crops based on soil, NPK, season, and climate |
| 💧 **Smart Irrigation** | AI-driven irrigation decisions based on soil moisture & weather |
| 🌦️ **Weather Intelligence** | Live weather + farming action recommendations |
| ♻️ **Sustainability Score** | Measure water, resource and crop health impact |
| 🤖 **AI Farmer Assistant** | Multilingual chatbot — English, Hindi, Gujarati |

## 📁 Project Structure

```text
AGRIVISION-AI/
├── backend/
│   ├── app/
│   │   ├── modules/
│   │   │   ├── disease_detection/
│   │   │   ├── crop_recommendation/
│   │   │   ├── smart_irrigation/
│   │   │   ├── smart_weather_based_Intelligence/
│   │   │   ├── sustainability/
│   │   │   ├── farmer_assistant/
│   │   │   └── agentic_advisor/
│   │   └── core/
│   └── requirements.txt
└── frontend/
    └── src/
        ├── pages/
        ├── components/
        └── services/
```

## Sample Dataset

A sample dataset containing test leaf images (healthy and diseased) and sample NPK/soil data for testing the recommendation engine is included in the project for demonstration.

## Tech Concepts Used

| Concept | Where |
| REST API and Routing | `backend/app/main.py` |
| Machine Learning Inference | `backend/app/modules/disease_detection/` |
| State Management | `frontend/src/components/` |
| File Upload Handling | `backend/app/core/` |
| External API Integration | `backend/app/modules/smart_weather_based_Intelligence/` |
| Exception Handling | All backend service classes |
| Component-based UI | `frontend/src/pages/` |

## Author

- Name: Akash Kumar Pandit
- ID: 24BAI10629
- Course: B.Tech Artificial Intelligence
- Institution: VIT Bhopal University
