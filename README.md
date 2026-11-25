# FLEX AI Life Coach

![FLEX AI Life Coach](assets/Flex_Header.png)

FLEX is a team graduation project for turning a user's goals and daily schedule into a productivity plan. The React interface pairs a guided planner with a chat assistant. A Python retrieval service searches study materials to give the assistant context for its responses.

## How the pieces fit

| Component | Where to look |
| --- | --- |
| Planner and chat screens | [React pages](src/pages) |
| HTTP routes and request models | [FastAPI service](src/services/api.py) |
| Document retrieval and model integration | [RAG system](src/services/rag_system.py) |
| Session and message persistence | [SQLite storage](src/services/chat_storage.py) |
| Agent experiments | [Project notebook](Flex_AI_Agent.ipynb) |

## Run locally

From the repository root, create a Python virtual environment, activate it, then run the commands below. Set `GOOGLE_API_KEY` in your local copy of `.env` before starting the API.

```sh
cp .env.example .env
python -m pip install -r requirements.txt
python -m uvicorn src.main:app --reload --port 8000
```

In a second terminal, start the frontend and open the URL Vite prints.

```sh
npm ci
npm run dev
```

## 👥 Team

- Mohamed Wael
- Mohamed Amr
- Kareem Nagah
- Amr Amgad
- Youssef Alsebaey
- Loay Ayman
- Abdallah Elhosseny
- Salma Gamal
- Tasneem Osama

