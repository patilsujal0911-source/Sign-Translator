# 🤟 Sign Translator 

Welcome! This is a beginner-friendly web app that helps you **translate** and **learn** American Sign Language (ASL) using nothing but your webcam.

Think of it like Google Translate, but for sign language — point your camera at your hands, and the app tells you what sign you're making.

**Author:** Sujal Patil

---

## 🎯 What Does This Do?

The app has three main features:

| Feature | What it does |
|---|---|
| 📹 **Real-Time Translator** | Point your webcam at your hands and the app recognizes ASL signs live, using an AI model trained on 250 signs. |
| 📚 **Learning Hub** | Browse, search, and study a catalog of 250+ ASL signs with details for each one. |
| 🔊 **Text-to-Speech** | Hear the meaning of a detected sign spoken out loud, right in your browser. |

---

## ⚡ Quick Start (Easiest Way)

### 🪟 Windows
1. Open the project folder.
2. Double-click **`run.bat`**.
3. Wait until you see `Running on http://localhost:5000` in the terminal.
4. Open your browser to **http://localhost:5000**.

### 🍎🐧 macOS / Linux
1. Open a terminal in the project folder.
2. Run:
   ```bash
   chmod +x run.sh
   ./run.sh
   ```
3. Open your browser to **http://localhost:5000**.

That's it — you're ready to go! 🎉

---

## 🔧 Manual Setup (If Quick Start Doesn't Work)

### Step 1 — Install Python
Download it from [python.org/downloads](https://www.python.org/downloads/). During installation, **check the box that says "Add Python to PATH."**

### Step 2 — Open a Terminal
- **Windows:** Press `Win + R`, type `cmd`, press Enter.
- **Mac/Linux:** Open the **Terminal** app.

### Step 3 — Navigate to the Project Folder
```bash
cd path/to/Sign-Translator
```

### Step 4 — Create a Virtual Environment
A virtual environment keeps this project's packages separate from everything else on your computer.

**Windows:**
```bash
python -m venv venv
venv\Scripts\activate
```

**Mac/Linux:**
```bash
python3 -m venv venv
source venv/bin/activate
```

You'll know it worked if you see `(venv)` at the start of your terminal line.

### Step 5 — Install the Required Packages
```bash
pip install -r requirements.txt
```
This may take 5–10 minutes the first time — it's downloading Flask, TensorFlow, OpenCV, and a few other tools.

### Step 6 — Start the App
```bash
python app.py
```

### Step 7 — Open Your Browser
Go to **http://localhost:5000** — you should see the home page.

---

## 📖 How to Use the App

### 🏠 Home Page
A quick overview of the project with links to the Translator and Learning Hub.

### 🎬 Translator Page
1. Click **"Start Translator"** to turn on your webcam.
2. Hold up your hands and make an ASL sign.
3. The app displays the detected sign and its meaning in real time.
4. Click **"Stop"** when you're done.
5. Toggle **"Text to Speech"** to hear the meaning spoken aloud.

**Tips for best results:**
- Use good, even lighting (natural light works great).
- Keep your hands and upper body fully in frame.
- Hold each sign steady for 2–3 seconds.
- Avoid busy backgrounds that make hands harder to detect.

### 📚 Learning Hub
- Browse all 250+ supported ASL signs.
- Type in the search box to find a specific sign instantly.
- Click any sign card to see more details.
- Press **`Ctrl + K`** to jump straight to the search box.

---

## 📁 Project Structure

```
Sign-Translator/
├── app.py                       ← Runs the Flask web application
├── INTERFACE.py                  ← Standalone reference script for ASL detection
├── requirements.txt              ← Packages this project needs
├── run.bat / run.sh              ← One-click setup & launch scripts
├── models/
│   └── FINAL_ASL_250.h5          ← The trained AI model (recognizes 250 signs)
├── src/
│   ├── backbone.py               ← AI model architecture
│   ├── landmarks_extraction.py   ← Detects hands, face & body landmarks
│   ├── config.py                 ← Model settings (thresholds, sequence length)
│   ├── utils.py                  ← Helper functions
│   └── sign_to_prediction_index_map.json   ← Maps signs to model output classes
├── templates/                    ← The web pages
│   ├── base.html                  (shared layout/navbar)
│   ├── index.html                 (home page)
│   ├── translator.html            (translator page)
│   └── learn.html                 (learning hub)
└── static/                       ← Styling, scripts & media
    ├── css/style.css
    ├── js/app.js
    └── videos/
```

---

## ⚙️ What Software Does This Need?

Everything is listed in `requirements.txt`, but here's the plain-English version:

| Package | What it's for |
|---|---|
| **Flask** | Powers the web app and pages |
| **OpenCV** | Reads your webcam feed |
| **MediaPipe** | Detects your hands, face, and body pose |
| **TensorFlow** | Runs the AI model that recognizes signs |
| **NumPy** | Handles the number-crunching behind the scenes |

You don't need to understand any of this — just run `pip install -r requirements.txt` and you're set.

---

## 🐛 Troubleshooting

| Problem | Fix |
|---|---|
| **"Port 5000 is already in use"** | Close any other app using that port, or open `app.py` and change `port=5000` to `port=5001`. |
| **Camera not working** | Make sure you allowed camera access in your browser, try a different browser, and confirm no other app is using the webcam. |
| **"Module not found" error** | Make sure your virtual environment is active (you should see `(venv)`), then run `pip install -r requirements.txt` again. |
| **"Python command not found"** | Reinstall Python and check "Add Python to PATH," or try `python3` instead of `python`. |
| **Translator feels slow or laggy** | Close other apps using the camera/CPU, and make sure you're in a well-lit room. |

---

## 🚀 Next Steps

Once the app is running:
1. ✅ Try the **Translator** — make a few ASL signs and watch it recognize them.
2. ✅ Explore the **Learning Hub** — search and browse the full 250-sign catalog.
3. ✅ Peek at the code in `app.py` and `src/` to see how it all works under the hood.

For a deeper technical breakdown of the Flask app, routes, and ML pipeline, check out **[README_FLASK.md](README_FLASK.md)**.

---

## ❓ Common Questions

**Q: Do I need to know sign language already?**
Nope — this app is built for learning. Use the Learning Hub to practice signs before testing them in the Translator.

**Q: Can I use this on my phone?**
The app works best on a computer with a webcam. Mobile support is limited for now.

**Q: Where does the AI model come from?**
It's a pre-trained model (`models/FINAL_ASL_250.h5`) trained to recognize 250 distinct ASL signs.

**Q: Can I add my own signs?**
Yes, but it requires retraining the model — that's an advanced task that needs some Python and ML experience.

---

## 📚 Learn More

- **ASL Learning:** [lifeprint.com](https://www.lifeprint.com/) — a great free ASL resource
- **Flask Docs:** [flask.palletsprojects.com](https://flask.palletsprojects.com/)
- **TensorFlow Docs:** [tensorflow.org](https://www.tensorflow.org/)

---

## 🎓 Project Info

- **Built with:** Python, Flask, TensorFlow, OpenCV, MediaPipe
- **Supports:** 250 American Sign Language (ASL) signs
- **Requires:** Python 3.8+ and a webcam
- **License:** MIT — see [LICENSE](LICENSE)

---

## 🙋 Author

**Sujal Patil**

Enjoy learning sign language! 🤟
