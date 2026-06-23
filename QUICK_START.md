# 🎯 QUICK START GUIDE

## ⚡ 30-Second Setup

### Windows
```bash
run.bat
```
Then open: http://localhost:5000

### macOS/Linux
```bash
chmod +x run.sh
./run.sh
```
Then open: http://localhost:5000

---

## 📋 Manual Setup (if scripts fail)

### Step 1: Create Virtual Environment
```bash
python -m venv venv
```

### Step 2: Activate Virtual Environment

**Windows:**
```bash
venv\Scripts\activate
```

**macOS/Linux:**
```bash
source venv/bin/activate
```

### Step 3: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 4: Run Application
```bash
python app.py
```

### Step 5: Open Browser
```
http://localhost:5000
```

---

## 🔍 Verify Installation

After running the app, you should see:
```
WARNING in app.run_simple
 * Running on http://0.0.0.0:5000
 * Press CTRL+C to quit
 * Restarting with reloader
 * Debugger is active!
```

If you see this, the app is running successfully! ✅

---

## 🌐 Access Points

| Page | URL | Purpose |
|------|-----|---------|
| Home | http://localhost:5000/ | Overview & navigation |
| Translator | http://localhost:5000/translator | Real-time translation |
| Learning | http://localhost:5000/learn | Browse 250 signs |

---

## 🎨 Features to Try

1. **Home Page**
   - Read project objectives
   - Learn about technology stack
   - Navigate to other pages

2. **Translator Page**
   - Click "Start Translation"
   - Allow camera access
   - See simulated sign detection
   - Enable text-to-speech

3. **Learning Hub**
   - Search for signs (try: "hello", "cat", "happy")
   - Filter by category
   - Click cards to see details
   - Practice and save signs

---

## 🛠️ Troubleshooting

### Port Already in Use
If port 5000 is already in use, modify `app.py`:
```python
if __name__ == '__main__':
    app.run(debug=True, host='0.0.0.0', port=5001)  # Change 5000 to 5001
```

### Module Not Found
```bash
pip install --upgrade pip
pip install -r requirements.txt
```

### Python Not Found
Ensure Python 3.8+ is installed and available in PATH:
```bash
python --version
```

---

## 📚 File Structure

```
SLT/
├── app.py                    ← Main Flask application
├── requirements.txt          ← Python dependencies
├── run.bat                   ← Windows startup script
├── run.sh                    ← macOS/Linux startup script
├── templates/                ← HTML files
│   ├── base.html            (Navigation, footer)
│   ├── index.html           (Home page)
│   ├── translator.html      (Translator interface)
│   └── learn.html           (Learning hub)
└── static/
    ├── css/
    │   └── style.css        (Neumorphism styling)
    └── js/
        └── app.js           (JavaScript functionality)
```

---

## 🚀 Next Steps

1. ✅ Run the app (`run.bat` or `run.sh` or `python app.py`)
2. ✅ Open http://localhost:5000 in your browser
3. ✅ Explore all three pages
4. ✅ Test the translator with camera
5. ✅ Browse and search signs in the learning hub

---

## 🔗 Integration with ML Model

The app is ready to integrate with the existing ML model:
- `FINAL_ASL_250.h5` in the models folder
- `INTERFACE.py` shows the backend logic
- Modify `translator.html` to use actual predictions instead of simulated ones

---

## 💡 Tips

- 🔍 Use Ctrl+K to quickly focus the search bar
- 🔊 Enable text-to-speech in the translator for spoken output
- 📱 The app is fully responsive - try it on mobile!
- 🎨 Colors and styles can be customized in `static/css/style.css`

---

Need help? Check `README_FLASK.md` for detailed documentation!
