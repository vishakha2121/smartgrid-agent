# 🧠⚡ GridMind-AI
### Multi-Agent AI Smart Energy Grid Optimization System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-0.100+-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black" />
  <img src="https://img.shields.io/badge/Gemini-AI-4285F4?style=for-the-badge&logo=google&logoColor=white" />
  <img src="https://img.shields.io/badge/SQLite-3-003B57?style=for-the-badge&logo=sqlite&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge" />
</p>

<p align="center">
  <b>A multi-agent AI system where 6 autonomous agents collaborate to optimize a smart energy grid in real-time.</b>
</p>

---

## 🌟 What is GridMind-AI?

**GridMind-AI** is a full-stack, multi-agent AI system that simulates and optimizes a **Smart Energy Grid**. It uses **6 autonomous AI agents** that reason, communicate, and make decisions in real-time to:

- ⚡ Balance electricity production & consumption
- ☀️ Integrate solar renewable energy intelligently
- 💨 Optimize wind turbine output
- 🔋 Manage battery storage charge/discharge cycles
- 🏠 Predict and respond to consumer demand
- 🚨 Detect outages and orchestrate recovery

Each agent is powered by **Google Gemini API** for reasoning and decision-making, combined with custom Python logic for numerical optimization.

> ⚠️ **Note**: This is a **practice/learning project**, not production-ready. It is designed to run on **CPU-only machines** by using cloud-based Gemini API instead of local LLMs.

---

## 🎯 Project Goals

This project was built as a **hands-on learning exercise** to master:

1. **Multi-Agent AI Architecture** — how autonomous agents collaborate and resolve conflicts
2. **LLM Integration** — using Gemini API for structured reasoning outputs
3. **Real-time Systems** — WebSocket-based live data streaming
4. **Full-Stack Development** — FastAPI backend + React frontend
5. **Energy Domain Knowledge** — smart grid concepts, load balancing, demand response
6. **Data Persistence** — SQLite with SQLAlchemy ORM
7. **Modern UI/UX** — dark "control room" dashboard with live charts

---

## 🤖 The 6 AI Agents

| # | Agent | Icon | Responsibility |
|---|-------|------|----------------|
| 1 | **Grid Agent** | 🔌 | Master orchestrator — balances overall grid load & supply |
| 2 | **Solar Agent** | ☀️ | Predicts solar production, manages PV panel output |
| 3 | **Wind Agent** | 💨 | Forecasts wind speed, optimizes turbine output |
| 4 | **Storage Agent** | 🔋 | Decides when to charge/discharge batteries |
| 5 | **Demand Agent** | 🏠 | Predicts consumer demand, triggers demand response |
| 6 | **Recovery Agent** | 🚨 | Detects outages, coordinates recovery plans |

All agents communicate through an **Orchestrator** that resolves conflicts and prioritizes actions based on grid health.

---

## 🏗️ System Architecture

```
┌─────────────────────────────────────────────────────────────┐
│                    React Frontend (Vite)                     │
│   Dashboard · Charts · Agent Logs · Live Metrics · Alerts    │
└──────────────────────────┬──────────────────────────────────┘
                           │ REST API + WebSocket
                           │ (Axios + native WS)
┌──────────────────────────▼──────────────────────────────────┐
│                    FastAPI Backend                           │
│                                                              │
│   ┌────────────────────────────────────────────────────┐    │
│   │              Agent Orchestrator                     │    │
│   │  ┌──────┐ ┌───────┐ ┌──────┐ ┌────────┐            │    │
│   │  │ Grid │ │ Solar │ │ Wind │ │Storage │            │    │
│   │  └──────┘ └───────┘ └──────┘ └────────┘            │    │
│   │  ┌────────┐ ┌──────────┐                            │    │
│   │  │ Demand │ │ Recovery │                            │    │
│   │  └────────┘ └──────────┘                            │    │
│   └────────────────────────────────────────────────────┘    │
│                           │                                  │
│                  ┌────────▼─────────┐                        │
│                  │  Gemini API      │  (reasoning)           │
│                  └────────┬─────────┘                        │
│                           │                                  │
│                  ┌────────▼─────────┐                        │
│                  │  SQLAlchemy ORM  │                        │
│                  └────────┬─────────┘                        │
│                           │                                  │
│                  ┌────────▼─────────┐                        │
│                  │   SQLite DB      │  (energy_grid.db)      │
│                  └──────────────────┘                        │
└──────────────────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

### Backend
| Tech | Purpose |
|------|---------|
| Python 3.10+ | Core language |
| FastAPI | REST API + WebSocket server |
| Uvicorn | ASGI server |
| SQLAlchemy | ORM |
| SQLite | Lightweight database |
| Google Gemini API | LLM reasoning for agents |
| Pydantic | Data validation |
| APScheduler | Agent background scheduling |
| Loguru | Structured logging |
| python-dotenv | Env variable management |
| Pandas / NumPy | Numerical processing |

### Frontend
| Tech | Purpose |
|------|---------|
| React 18 | UI framework |
| Vite | Fast build tool |
| Tailwind CSS | Utility-first styling |
| shadcn/ui | Pre-built components |
| Recharts | Charts & graphs |
| Zustand | Lightweight state management |
| Axios | HTTP client |
| Framer Motion | Animations |
| Lucide React | Icon library |
| React Router v6 | Routing |
| React Hot Toast | Notifications |

### DevOps (optional)
- Docker & docker-compose
- GitHub Actions (CI)
- Git & GitHub

---

## ✨ Features

- ✅ **6 Autonomous AI Agents** with Gemini reasoning
- ✅ **Real-time Dashboard** with live grid metrics
- ✅ **Interactive Charts** — production, demand, storage trends
- ✅ **Agent Decision Feed** — see what each agent is thinking
- ✅ **Energy Flow Diagram** — visual grid topology
- ✅ **Outage Simulation** — trigger & watch recovery in action
- ✅ **WebSocket Live Updates** — no page refresh needed
- ✅ **Dark "Control Room" UI** — sleek, modern, professional
- ✅ **Auto-generated API Docs** — Swagger UI at `/docs`
- ✅ **SQLite Persistence** — all events, logs, decisions saved
- ✅ **Agent Chat** — ask agents questions, get reasoned answers
- ✅ **Simulation Mode** — mock data for demo without sensors

---

## 🚀 Quick Start

### Prerequisites
- **Python 3.10+** — [Download](https://www.python.org/downloads/)
- **Node.js 18+** — [Download](https://nodejs.org/)
- **Gemini API Key** — [Get here](https://aistudio.google.com/apikey)
- **Git** — [Download](https://git-scm.com/)

### 1️⃣ Clone the Repository

```bash
git clone https://github.com/vishakha2121/smartgrid-agent.git
cd smartgrid-agent
```

### 2️⃣ Backend Setup

```bash
cd backend

# Create virtual environment
python -m venv venv

# Activate (Windows)
venv\Scripts\activate

# Activate (Mac/Linux)
# source venv/bin/activate

# Install dependencies
pip install -r requirements.txt

# Setup environment variables
copy .env.example .env
# Then edit .env and add your GEMINI_API_KEY

# Run the backend
uvicorn main:app --reload --port 8000
```

Backend will run at **http://localhost:8000**
API Docs at **http://localhost:8000/docs**

### 3️⃣ Frontend Setup

Open a **new terminal**:

```bash
cd frontend

# Install dependencies
npm install

# Setup env
copy .env.example .env

# Run dev server
npm run dev
```

Frontend will run at **http://localhost:5173**

### 4️⃣ Open the Dashboard

Go to **http://localhost:5173** in your browser 🎉

---

## 📁 Project Structure

```
gridmind-ai/
│
├── README.md
├── .gitignore
├── .env.example
├── LICENSE
├── docker-compose.yml
│
├── docs/                          # Documentation
│   ├── architecture.png
│   ├── agent_flow.md
│   ├── api_reference.md
│   └── setup_guide.md
│
├── backend/                       # Python FastAPI backend
│   ├── requirements.txt
│   ├── .env
│   ├── main.py
│   ├── config.py
│   ├── database.py
│   ├── app/
│   │   ├── agents/                # 6 AI agents
│   │   ├── services/              # Gemini, simulation, WS
│   │   ├── api/v1/                # REST routes
│   │   ├── models/                # SQLAlchemy models
│   │   ├── schemas/               # Pydantic schemas
│   │   ├── core/                  # Config, logger, security
│   │   ├── utils/                 # Helpers
│   │   └── data/                  # Seed & mock data
│   ├── database/                  # SQLite + migrations
│   ├── tests/                     # Pytest
│   └── logs/
│
├── frontend/                      # React + Vite
│   ├── package.json
│   ├── vite.config.js
│   ├── tailwind.config.js
│   ├── index.html
│   ├── public/
│   └── src/
│       ├── api/
│       ├── components/
│       ├── pages/
│       ├── hooks/
│       ├── context/
│       ├── store/
│       ├── utils/
│       └── styles/
│
├── database/                      # SQL schemas & backups
│   ├── schema.sql
│   └── energy_grid.db
│
└── scripts/                       # Utility scripts
    ├── start_backend.sh
    ├── start_frontend.sh
    ├── seed_database.py
    ├── run_simulation.py
    └── test_gemini.py
```

---

## 🔑 Environment Variables

### Backend `.env`
```env
GEMINI_API_KEY=your_gemini_api_key_here
DATABASE_URL=sqlite:///./database/energy_grid.db
APP_ENV=development
LOG_LEVEL=INFO
CORS_ORIGINS=http://localhost:5173
```

### Frontend `.env`
```env
VITE_API_BASE_URL=http://localhost:8000/api/v1
VITE_WS_URL=ws://localhost:8000/ws
```

---

## 🎓 Learning Outcomes

By building this project, I learned:

- ✅ Multi-agent system design patterns
- ✅ LLM prompt engineering for structured JSON outputs
- ✅ WebSocket-based real-time communication
- ✅ FastAPI async patterns & dependency injection
- ✅ React state management at scale (Zustand)
- ✅ Energy domain modeling (load, generation, storage)
- ✅ Full-stack integration & CORS handling
- ✅ Database schema design for time-series data

---

## 🧪 Testing

### Backend Tests
```bash
cd backend
pytest
```

### Manual API Test
```bash
curl http://localhost:8000/api/v1/grid/status
```

---

## 🤝 Contributing

This is a personal learning project, but suggestions and improvements are welcome!

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

## 👨‍💻 Author

**Vishakha**
- GitHub: [@vishakha2121](https://github.com/vishakha2121)
- Project Repo: [smartgrid-agent](https://github.com/vishakha2121/smartgrid-agent)

---

## 🙏 Acknowledgements

- [Google Gemini API](https://ai.google.dev/) for LLM reasoning
- [FastAPI](https://fastapi.tiangolo.com/) for the backend framework
- [React](https://react.dev/) & [Vite](https://vitejs.dev/) for frontend
- [Tailwind CSS](https://tailwindcss.com/) for styling
- [Recharts](https://recharts.org/) for beautiful charts

---

<p align="center">
  ⭐ <b>Star this repo if you found it interesting!</b> ⭐
</p>

<p align="center">
  Made with ❤️ and ⚡ by Vishakha
</p>