# Eight Ways API

Backend of **Eight Ways**, a habit-tracking app based on the 8 natural remedies of Ellen G. White. It is made of two Python services: a goals CRUD API and **Lumin**, a chatbot that answers questions about the remedies and helps users change habits.

> Mobile app: [eight-ways-mobile](https://github.com/Joao-Adegas/eight-ways-mobile)

## Services

| Service | Purpose | Port |
|---|---|---|
| Chatbot (Lumin) | Answers questions about the natural remedies and supports habit change | 5000 |
| Goals CRUD | Users' personalized goals and daily progress | 8000 |

## Tech stack

Python, FastAPI, Uvicorn, LangChain, langchain-groq

## Getting started

### Prerequisites

- Python
- Libraries listed in each service's `requirements.txt`

<!-- CONFIRM: the chatbot probably needs a GROQ_API_KEY in a .env file; document it here if so -->

### Run each service

Open the folder of the service and run the steps below. Do this once for the chatbot and once for the goals CRUD.

```bash
python -m venv env

# Windows
./env/Scripts/activate
# macOS / Linux
source env/bin/activate

pip install -r requirements.txt
```

Chatbot:

```bash
uvicorn main:app --host 0.0.0.0 --port 5000 --reload
```

Goals CRUD:

```bash
uvicorn main:app --host 0.0.0.0 --port 8000 --reload
```

Example endpoint used by the app:

```
http://<YOUR_IP>:8000/usuarios/1/objetivos_personalizados/
```

## Future work

- Individual screens for each natural remedy
- Better real-time updates
- A more precise Lumin chatbot
- Production deployment

## Team

- Gabriela Alejandra Bergamine dos Santos
- João Pedro dos Santos Adegas — [@Joao-Adegas](https://github.com/Joao-Adegas)
- Pedro Sérgio

Project developed for the Hackathon 2025 – Unasp Tech.
