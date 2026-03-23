# MedSafe AI – AI-Driven Medical Safety Assistant + Fitness

A fully self-contained Streamlit web application for medication safety and personal health management.

## Features

| Module | Description |
|---|---|
| 🏠 Dashboard | Stats, quick access cards, active profile medicines, recent logs |
| 💊 Medicine Interactions | Fuzzy-match medicines and check for drug-drug interactions |
| 📷 Prescription Scanner | OCR scan a prescription image to detect medicine names |
| 🩺 Symptom Guide | Educational guidance on 8 common symptoms |
| 📋 Side Effect Monitor | Log and track medication side effects per profile |
| 🚨 Emergency Risk Predictor | Keyword-based risk assessment (HIGH / MODERATE / LOW) |
| 🏃 Fitness Guide | Exercise, yoga, diet, hydration, and sleep tips |
| 👥 Profile Manager | Multi-profile support for family members |

## Requirements

- Python 3.9+
- Streamlit
- fuzzywuzzy + python-Levenshtein
- Pillow
- pytesseract (optional – app works without it, falls back to demo mode)

## Installation

```bash
pip install -r requirements.txt
```

For OCR scanning (Prescription Scanner), you also need Tesseract OCR installed on your system:
- **Linux:** `sudo apt install tesseract-ocr`
- **macOS:** `brew install tesseract`
- **Windows:** Download from https://github.com/UB-Mannheim/tesseract/wiki

## Running the App

```bash
streamlit run app.py
```

The app will open at `http://localhost:8501` by default.

## Notes

- All data is hardcoded in Python — no database or API calls required.
- All state is managed with `st.session_state`.
- Medical information is for **educational purposes only** and does not constitute medical advice.
- If pytesseract is not installed, the Prescription Scanner shows a demo result instead of crashing.