# 🎯 AI Interview Coach

An AI-powered mock interview platform that simulates a real technical interview experience — with live question generation, answer evaluation, instant feedback, and session analytics.

Built with vanilla HTML, CSS, JavaScript and powered by the **Anthropic Claude API**.

---

## 📸 Features

- 🤖 **AI Interviewer** — Realistic video-call UI with animated avatar, speaking indicators, and typewriter question delivery
- ⏱️ **Countdown Timer** — 2-minute limit per question, just like a real interview
- 📝 **Smart Feedback** — Per-answer scoring (1–10), strengths, improvements, and suggested talking points
- 📊 **Session Analytics** — Final score arc, progression chart, and full question breakdown
- 🎭 **6 Roles** — Full Stack, Frontend, Backend, DSA, System Design, DevOps
- 🔴 **3 Difficulty Levels** — Easy, Medium, Hard
- 💡 **Quick Tips** — Inline answer starters to help structure responses
- 📱 **Responsive** — Works on desktop and mobile

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| Frontend | HTML5, CSS3, Vanilla JavaScript (ES6+) |
| AI Engine | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Fonts | Inter, JetBrains Mono (Google Fonts) |
| Deployment | Any static host (GitHub Pages, Netlify, Vercel) |

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/ai-interview-coach.git
cd ai-interview-coach
```

### 2. Get Your Anthropic API Key

1. Go to [console.anthropic.com](https://console.anthropic.com)
2. Sign up or log in
3. Navigate to **API Keys** → **Create Key**
4. Copy your key (starts with `sk-ant-api03-...`)

> ⚠️ Anthropic gives free credits on signup — enough for many interview sessions.

### 3. Run the App

Simply open the file in your browser:

```bash
# Option 1 — double-click the file
open ai-interview-coach.html

# Option 2 — use a local server
npx serve .
# or
python -m http.server 8000
```

### 4. Start Practicing

1. Paste your API key into the input field
2. Choose your role and difficulty
3. Click **Start Interview Session**
4. Answer 5 questions and get your score!

---

## 📁 Project Structure

```
ai-interview-coach/
│
├── ai-interview-coach.html   # Complete app (HTML + CSS + JS in one file)
└── README.md                 # Project documentation
```

> The entire app is contained in a single HTML file — no build tools, no dependencies, no setup required.

---

## 🎮 How It Works

```
User Selects Role & Difficulty
           │
           ▼
  App calls Claude API
  → "Generate a [Role] interview question at [Difficulty] level"
           │
           ▼
  Question types out letter-by-letter
  + 2-minute timer starts
           │
           ▼
  User types their answer
           │
           ▼
  App calls Claude API again
  → "Evaluate this answer, score it 1-10, give feedback"
           │
           ▼
  Feedback modal appears
  (Score, Verdict, Strengths, Improvements, Talking Point)
           │
           ▼
  Repeat for 5 questions
           │
           ▼
  Final Results Screen
  (Avg score, chart, full breakdown)
```

---

## 🔧 Configuration

You can customize the following constants at the top of the `<script>` section:

```javascript
const TOTAL = 5;          // Number of questions per session
const ROLES = [...];      // Add or remove interview roles
// Timer is set to 120 seconds per question (inside startTimer())
```

---

## 🌐 Deployment

### GitHub Pages

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/your-username/ai-interview-coach.git
git push -u origin main
# Then enable GitHub Pages in repo Settings → Pages → main branch
```

### Netlify

```bash
# Drag and drop the ai-interview-coach.html file at netlify.com/drop
```

### Vercel

```bash
npx vercel --prod
```

---

## 🔒 Security Notes

- Your API key is **never stored** — it lives only in the browser session
- The key is sent directly from your browser to the Anthropic API
- For production use, consider building a backend proxy (Node.js + Express) to keep the key server-side

---

## 🗺️ Roadmap

- [ ] Voice input support (Web Speech API)
- [ ] PDF report export after session
- [ ] Backend proxy server (Node.js) for secure API key handling
- [ ] User accounts + session history
- [ ] Leaderboard with score comparisons
- [ ] Resume-based question generation (upload your CV)
- [ ] Interview recording & playback

---

## 👤 Author

**Zaid Ali**
- GitHub: [@zaidali](https://github.com/zaidali)
- LinkedIn: [linkedin.com/in/zaidali](https://linkedin.com/in/zaidali)
- Email: zaidali.za2635@gmail.com
- Portfolio: [your-portfolio.com](https://your-portfolio.com)

---

## 📄 License

This project is licensed under the **MIT License** — feel free to use, modify, and distribute it.

```
MIT License — Copyright (c) 2025 Zaid Ali
Permission is hereby granted, free of charge, to any person obtaining a copy
of this software to use, copy, modify, merge, and distribute freely.
```

---

## 🙏 Acknowledgements

- [Anthropic](https://anthropic.com) — for the Claude API
- [Google Fonts](https://fonts.google.com) — Inter & JetBrains Mono
- Inspired by real technical interview experiences 🎯

---

<p align="center">⭐ If this helped you, give it a star on GitHub!</p>
