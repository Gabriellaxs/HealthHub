# HealthHub — Applicazione Full-Stack per la Gestione Ospedaliera

> **Project Work** — CdS Informatica per le Aziende Digitali (L-31)
> Traccia PW 16 · Università Telematica Pegaso
> Settori: Informatica (INF/01) · Ingegneria Economico-Gestionale (ING-IND/35)

---

## Descrizione

**HealthHub** è un'applicazione web full-stack API-based sviluppata per un'organizzazione del settore sanitario. Il sistema gestisce le principali attività di un ospedale, offrendo funzionalità di:

- Prenotazione visite e gestione appuntamenti
- Gestione referti medici
- Amministrazione di medici, pazienti, sedi e reparti
- Gestione ricoveri, operazioni e turni
- Teleconsulenze
- Dashboard statistiche per ruolo (Paziente, Medico, Amministratore)

---

## Architettura

```
healthhub/
├── frontend/   → React 19 + TypeScript + Vite + Material UI
└── backend/    → Python + FastAPI + SQLAlchemy + SQLite
```

L'applicazione adotta un'architettura **RESTful API-based**: il frontend comunica con il backend tramite chiamate HTTP/JSON, con autenticazione **JWT (Bearer Token)**.

---

## Repository

| Componente | Tecnologie | Link |
|---|---|---|
| **Frontend** | React 19, TypeScript, Vite, MUI 7, React Router 7 | [HealthHubFrontend](https://github.com/Gabriellaxs/HealthHubFrontend) |
| **Backend** | Python, FastAPI, SQLAlchemy, SQLite, JWT | [HealthHubBackend](https://github.com/Gabriellaxs/HealthHubBackend) |

---

## Stack Tecnologico

### Frontend
- **Framework:** React 19 + TypeScript
- **Build tool:** Vite
- **UI Library:** Material UI (MUI) v7
- **Routing:** React Router v7
- **HTTP Client:** Axios
- **Autenticazione:** JWT in localStorage

### Backend
- **Framework:** FastAPI (Python)
- **ORM:** SQLAlchemy
- **Database:** SQLite
- **Autenticazione:** OAuth2 + JWT (`python-jose`)
- **Hashing password:** bcrypt
- **Documentazione API:** Swagger UI (integrato in FastAPI — `/docs`)

---

## Funzionalità per ruolo

| Ruolo | Funzionalità |
|---|---|
| **Paziente** | Visualizza prenotazioni, referti, storico visite, teleconsulenze |
| **Medico** | Gestione agenda, referti, turni, operazioni, teleconsulenze |
| **Amministratore** | CRUD completo su tutte le entità del sistema |

---

## Avvio in locale

### Backend
```bash
cd healthhub-backend
python -m venv venv
venv\Scripts\activate        # Windows
pip install -r requirements.txt
uvicorn app.main:app --reload
# API disponibile su http://127.0.0.1:8000
# Documentazione Swagger: http://127.0.0.1:8000/docs
```

### Frontend
```bash
cd healthhub-frontend
npm install
npm run dev
# App disponibile su http://localhost:5173
```

---

## Documentazione API

La documentazione completa delle API REST è disponibile tramite **Swagger UI** integrato in FastAPI:

```
http://127.0.0.1:8000/docs
```

---

*Project Work — Università Telematica Pegaso · 2025/2026*
