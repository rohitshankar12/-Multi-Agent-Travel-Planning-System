# ✈️ Multi-Agent Travel Planning System

> An AI-powered travel planning system that transforms natural language travel requests into complete travel plans using multiple AI agents built with **LangGraph**, **LangChain**, **FastAPI**, and **Groq LLM**.

<p align="center">

![Python](https://img.shields.io/badge/Python-3.10+-3776AB?style=for-the-badge&logo=python&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white)
![LangGraph](https://img.shields.io/badge/LangGraph-Multi--Agent-blueviolet?style=for-the-badge)
![LangChain](https://img.shields.io/badge/LangChain-AI-success?style=for-the-badge)
![Groq](https://img.shields.io/badge/Groq-LLM-black?style=for-the-badge)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-Database-4169E1?style=for-the-badge&logo=postgresql&logoColor=white)

</p>

---

## 📖 Overview

Planning a trip often requires switching between airline websites, hotel booking platforms, travel blogs, and itinerary planners.

This project simplifies the entire process using a **multi-agent AI architecture**. A user's travel request is divided into specialized tasks handled by independent AI agents that collaborate to generate a personalized travel plan.

The system automatically provides:

- ✈️ Flight suggestions
- 🏨 Hotel recommendations
- 📅 Day-by-day itinerary
- 💰 Budget-aware planning
- 🍽 Travel recommendations
- 📝 Complete travel guide

---

## 🚀 Example

### User Prompt

```text
Plan a 5-day trip to Bali from Delhi with a budget of ₹60,000 including beach activities and local food.
```

### Generated Response

- Best available flights
- Hotel recommendations
- Daily itinerary
- Estimated expenses
- Tourist attractions
- Local food recommendations

---

# 🧠 Multi-Agent Workflow

```text
                   User Request
                        │
                        ▼
          Travel Coordinator Agent
                        │
      ┌─────────────────┼─────────────────┐
      │                 │                 │
      ▼                 ▼                 ▼
 Flight Agent      Hotel Agent     Itinerary Agent
      │                 │                 │
      └─────────────────┼─────────────────┘
                        ▼
         Response Formatting Agent
                        │
                        ▼
          Complete Travel Plan
```

---

# ✨ Features

- AI-powered travel planning
- Multi-Agent workflow using LangGraph
- Flight search using AviationStack API
- Hotel recommendations via Tavily Search
- AI-generated travel itineraries
- Budget-aware planning
- Conversation memory using PostgreSQL
- FastAPI REST backend
- Responsive web interface
- Modular architecture for easy extension

---

# 🛠 Tech Stack

| Category | Technology |
|----------|------------|
| Language | Python 3.10+ |
| Backend | FastAPI |
| AI Framework | LangChain |
| Agent Framework | LangGraph |
| LLM | Groq |
| Database | PostgreSQL |
| Flight API | AviationStack |
| Search API | Tavily |
| Frontend | HTML, CSS, JavaScript, Jinja2 |

---

# 📂 Project Structure

```text
Multi-Agent-Travel-Planning-System/
│
├── app.py
├── backend.py
├── requirements.txt
├── .env
│
├── static/
│   ├── css/
│   ├── js/
│   
│
├── templates/
│   └── index.html
│
└── tools/
    ├── flight_tool.py
    ├── tavily_tool.py
    
```

---

# ⚙️ Prerequisites

Before running the project, install:

- Python 3.10+
- PostgreSQL
- Git

Create API keys for:

- Groq
- Tavily
- AviationStack

---

# 🔑 Environment Variables

Create a `.env` file.

```env
DATABASE_URL=postgresql://user:password@localhost:5432/travel_db

GROQ_API_KEY=your_groq_api_key

AVIATIONSTACK_API_KEY=your_aviationstack_api_key

TAVILY_API_KEY=your_tavily_api_key

DEFAULT_ORIGIN_IATA=DEL
```

---

# 📦 Installation

### Clone Repository

```bash
git clone https://github.com/rohitshankar12/Multi-Agent-Travel-Planning-System.git

cd Multi-Agent-Travel-Planning-System
```

### Create Virtual Environment

```bash
python -m venv .venv
```

### Activate

Windows

```bash
.venv\Scripts\activate
```

Linux/macOS

```bash
source .venv/bin/activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run the Project

```bash
python app.py
```

Open

```
http://127.0.0.1:8000
```

---

# 📡 API Endpoints

## Health Check

```http
GET /health
```

## Generate Travel Plan

```http
POST /api/travel
```

Example

```bash
curl -X POST http://127.0.0.1:8000/api/travel \
-H "Content-Type: application/json" \
-d '{"message":"Plan a 3-day trip to Tokyo with a budget of $1200"}'
```

---

# 🔄 Workflow

1. User submits a travel request.
2. Coordinator Agent analyzes the request.
3. Flight Agent retrieves available flights.
4. Hotel Agent searches accommodation.
5. Itinerary Agent generates a personalized schedule.
6. Response Agent combines all outputs.
7. Final travel plan is returned to the user.
 
 ---

# 🎯 Future Improvements

- 🌦 Weather forecasting
- 🗺 Google Maps integration
- 💱 Currency conversion
- 🚖 Local transportation
- 🍽 Restaurant recommendations
- 📄 PDF itinerary export
- 🎤 Voice-enabled planning
- 📅 Google Calendar integration
- ❤️ Save favorite trips
- 🌍 Multi-language support

---

# 🤝 Contributing

Contributions are welcome.

1. Fork the repository
2. Create a feature branch

```bash
git checkout -b feature/new-feature
```

3. Commit changes

```bash
git commit -m "Add new feature"
```

4. Push branch

```bash
git push origin feature/new-feature
```

5. Open a Pull Request

---

# 📄 License

This project is licensed under the **MIT License**.

---

# 👨‍💻 Author

**Rohit Shankar**

B.Tech Electronics & Communication Engineering (AI/ML Specialization)

GitHub: **https://github.com/rohitshankar12**

---

# ⭐ Support

If you found this project useful, consider giving it a **Star ⭐** on GitHub.

It motivates future development and helps others discover the project.