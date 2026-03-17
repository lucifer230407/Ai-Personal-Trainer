# 🏋️ AI Personal Trainer

An AI-powered fitness trainer that uses your webcam to track body movements in real-time and automatically count reps for exercises like **bicep curls** and **squats** — no wearables needed.

## 🎥 Demo
> Run the app, stand in front of your webcam, and start working out. The trainer tracks your joints and counts your reps live.

---

## ✨ Features

- 📷 Real-time pose detection using **MediaPipe**
- 💪 **Bicep curl** rep counter
- 🦵 **Squat** rep counter
- 📐 Live joint angle display on screen
- 🎯 Stage tracking (up/down) for accurate rep counting

---

## 🛠️ Tech Stack

- **Python 3.11**
- **OpenCV** — webcam feed and frame rendering
- **MediaPipe** — pose landmark detection
- **NumPy** — angle calculations

---

## ⚙️ Installation

**1. Clone the repository**
```bash
git clone https://github.com/lucifer230407/Ai-Personal-Trainer.git
cd Ai-Personal-Trainer
```

**2. Create a virtual environment**
```bash
python -m venv venv
source venv/bin/activate        # Mac/Linux
venv\Scripts\activate           # Windows
```

**3. Install dependencies**
```bash
pip install -r requirements.txt
```

---

## ▶️ Usage
```bash
python trainer.py
```

- Stand **2-3 feet** from your webcam
- Make sure your **full body is visible** for squats
- Make sure your **left arm is visible** for bicep curls
- Press **`q`** to quit

---

## 📐 How It Works

The app uses MediaPipe to detect 33 body landmarks in real time. For each exercise, it calculates the angle between three key joints:

| Exercise | Joints Used |
|---|---|
| Bicep Curl | Shoulder → Elbow → Wrist |
| Squat | Hip → Knee → Ankle |

A rep is counted when the joint angle crosses the defined thresholds, completing a full range of motion.

---

## 📁 Project Structure
```
Ai-Personal-Trainer/
│
├── trainer.py          # Main application
├── requirements.txt    # Dependencies
└── README.md
```

---

## 🚧 Future Improvements

- [ ] Right arm support for bicep curls
- [ ] More exercises (push-ups, lunges, shoulder press)
- [ ] Voice feedback for rep counts
- [ ] Workout session summary
- [ ] Form correction alerts

---

## 👤 Author

**Himanshu Jangra**  
GitHub: [@lucifer230407](https://github.com/lucifer230407)

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
