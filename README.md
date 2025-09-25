# 📚 AI-Driven Adaptive Assessment Platform

This platform offers a personalized learning experience using **AI models**, **Q-learning**, and **Fog Computing**. It dynamically generates quizzes based on user performance and serves them efficiently through edge fog nodes.

---

## 🚀 Features

- 🎥 Extracts learning content from **YouTube videos**
- 🧠 Transcribes video using **Whisper**
- ✍️ Generates contextual quizzes using **Gemini (Google GenAI)**
- 🎯 Adapts difficulty with **Q-learning** (Reinforcement Learning)
- ⚙️ Uses **Fog Computing** for low-latency quiz delivery
- ⭐ Progress tracking, star-based rewards & user dashboards
- 📊 Personalized performance analytics

---

## 🛠️ Tech Stack

| Layer     | Tools Used                           |
|-----------|---------------------------------------|
| Frontend  | React (Vite) + Shadcn UI + Tailwind CSS |
| Backend   | Django REST Framework + JWT Auth      |
| AI Models | Whisper, Gemini (Google GenAI), Q-learning |
| Edge      | Flask Fog Server with local caching   |
| Data      | PostgreSQL (default), JSON-based Q-tables |
| DevOps    | Docker (for Flask), systemd services |

---

## 🧠 Models Used

| Model       | Purpose                    | Accuracy |
|-------------|----------------------------|----------|
| Whisper     | Audio Transcription        | ~90–95% (English, clear audio) |
| Gemini      | MCQ Question Generation    | ~85–92% (context relevance) |
| Q-learning  | Adaptive Difficulty Engine | ~90%+ (convergence accuracy) |

---

## 🔄 System Architecture

This AI-Driven Adaptive Assessment system combines Django (backend), React (frontend), and Flask (fog computing) to create a real-time, personalized quiz experience powered by AI models.

### 🎯 High-Level Flow

1. **User selects a course** → Selects a video to learn.
2. **Video Transcription** → Whisper (OpenAI) transcribes the audio.
3. **Quiz Generation** → Gemini API creates personalized questions based on Q-table difficulty and transcript context.
4. **Adaptive Quiz Delivery** → Questions are served based on user’s Q-learning performance via fog node.
5. **Result Analysis** → Scores, star rewards, progress, and adaptation level are stored and visualized.



### 🔧 Setup And Run

```bash
python -m venv env
source env/bin/activate
cd AiAdaptiveQuizBackend
pip install -r requirements.txt
python manage.py makemigrations
python manage.py migrate
python manage.py runserver
```

### 🔧 Packages (Django)
- Django + Django REST Framework
- Q-learning (Reinforcement Learning)
- Gemini (Google GenAI) for question generation
- Whisper (OpenAI) for transcription
- JWT Authentication
- Media handling with Pillow
- Documentation with drf-yasg



### 🔧 Setup And Run
```bash
cd AiQuizFrontend/
npm install
npm run dev
```

### 🔧 Packages
- Vite + React + TypeScript
- Tailwind CSS + ShadCN UI
- Redux Toolkit for state management
- Axios for API requests
- React Router



## ☁️ Fog Node (Flask)

### 🔧 Setup And Run
```bash
cd fog_computing/
pip install -r requirements.txt
python app.py
```

- Flask server acting as fog node
- Smart caching & log-based monitoring
- Low-latency API proxy for dashboard st



### 🛡️ Endpoints Cached via Fog Node

- /dashboard-info
- /total-stars
- /q-table/overall

## 🧪 How It Works

1. User selects a **Course** and starts a **Video**.
2. On video completion:
   - 🎙️ **Whisper** transcribes audio to text.
   - 🧠 **Gemini** (Google GenAI) generates context-aware questions based on transcript and Q-table difficulty.
   - 📊 **Q-learning engine** selects optimal difficulty level.
   - 🚀 Questions are delivered via **Flask Fog Node** (with caching).
3. 📝 User answers the quiz. Results are saved.
4. 🔁 Q-table is updated based on performance.
5. 📈 Dashboard reflects:
   - Progress per Course
   - Earned Rewards (🌟 Stars)
   - Quiz difficulty adaptation
   - Video-wise performance analytics


---

## 📊 Quiz Analysis & Adaptation

- 🎯 **Q-table is maintained per user per course**.
- 🔍 Each quiz session stores:
  - Difficulty served
  - Correct/wrong answers
  - Adaptation level (average Q-value)
- 📉 **Next questions adjust dynamically**.
- 📊 **Visual analytics**:
  - Course progress
  - Session-wise improvement
  - Difficulty trends

---

## 📈 Future Enhancements
- 🏅 Gamification with badges and achievements
- 🧩 More Quiz Types: Fill-in-the-blanks, Matching, True/False
- 🤖 AI Suggestions: Personalized topic recommendations
- 🧑‍🤝‍🧑 Peer Learning: Group-based quiz sessions

## 📬 Contact
Made with ❤️ by N. Venkat Swaroop

Email: venkatnvs2005@gmail.com

👉 [GitHub](https://github.com/venkatnvs) | [LinkedIn](https://www.linkedin.com/in/n-venkat-swaroop/)
