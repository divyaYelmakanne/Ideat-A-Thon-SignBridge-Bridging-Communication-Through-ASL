# GestureX: Real-Time American Sign Language (ASL) Recognition

GestureX (formerly Signify) is a web application that bridges communication barriers by providing real-time American Sign Language (ASL) recognition using AI and computer vision. The system leverages a webcam, MediaPipe Hands, and a machine learning model to detect and translate ASL gestures into text.

---

## Features
- **Live ASL Detection:** Recognizes ASL alphabet signs in real-time using your webcam.
- **Sentence Formation:** Forms sentences as you sign multiple characters.
- **Text-to-Speech:** Converts recognized sentences to speech.
- **Learning Mode:** Learn ASL alphabets with visual guides.
- **Modern UI:** Clean, professional, and responsive design.

---

## Folder Structure
```
Signify-main/
  ├── assests/
  │   ├── asl/           # ASL alphabet images
  │   └── images/        # UI images
  ├── backend/
  │   ├── app.py         # Flask backend (API)
  │   ├── model.p        # Trained ML model
  │   ├── ...            # Data scripts, helpers
  └── frontend/
      ├── index.html     # Home page
      ├── detect.html    # Live detection page
      ├── learn.html     # ASL learning page
      ├── contact.html   # Contact page
      ├── script.js      # Frontend logic
      └── style.css      # Stylesheet
```

---

## Getting Started

### 1. **Clone the Repository**
```
git clone <repo-url>
cd Signify-main
```

### 2. **Backend Setup**
- **Requirements:** Python 3.7+
- **Install dependencies:**
  ```
  pip install flask flask-cors joblib scikit-learn
  ```
- **Run the backend:**
  ```
  cd backend
  python app.py
  ```
- The backend will start at `http://127.0.0.1:5000/` (used for API calls only).

### 3. **Frontend Setup**
- **Requirements:** Modern web browser, Python (for local server)
- **Start a local server:**
  ```
  cd ../frontend
  python -m http.server 8000
  ```
- **Open in browser:**
  Go to [http://localhost:8000/detect.html](http://localhost:8000/detect.html)

---

## Usage
1. **Start both backend and frontend servers.**
2. **Open the detection page** in your browser.
3. **Allow webcam access** when prompted.
4. **Show ASL signs** (A-Z, space) in front of your webcam.
5. **Detected character** and **formed sentence** will appear on the page.
6. Use the **Reset**, **Backspace**, and **Speak** buttons as needed.

---

## Requirements
- Python 3.7+
- Flask
- Flask-CORS
- joblib
- scikit-learn
- MediaPipe Hands (via CDN in frontend)

---

## Troubleshooting
- **404 Not Found on backend:** This is normal if you visit `127.0.0.1:5000` directly. The backend only serves the `/predict` API.
- **CORS or network errors:** Make sure you use a local server for the frontend (not `file://`).
- **ModuleNotFoundError:** Install missing Python packages with `pip install ...`.
- **Model errors:** Ensure `model.p` is present in the `backend/` folder.
- **No detection:** Check browser console and backend terminal for errors.

---

## Credits
- ASL images and references: [Your sources here]
- Built with Flask, MediaPipe, and scikit-learn
- UI inspired by modern accessibility and design best practices

---

## License
[MIT License or your preferred license] 