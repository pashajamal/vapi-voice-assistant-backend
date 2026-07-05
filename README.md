# 🎙️ VAPI Voice Assistant Backend

A FastAPI tool server for a VAPI-powered voice assistant to manage **todos**, **reminders**, and **calendar events** via SQLite.

## Tech Stack
- **FastAPI** — API framework
- **SQLAlchemy + SQLite** — ORM & database
- **Pydantic** — request validation
- **VAPI** — voice AI platform

## Setup

```bash
git clone https://github.com/<your-username>/vapi-voice-assistant-backend.git
cd vapi-voice-assistant-backend
pip install -r requirements.txt
uvicorn main:app --reload
```

## Endpoints

| Endpoint | Tool Name | Action |
|---|---|---|
| `POST /create_todo/` | `createTodo` | Create todo |
| `POST /get_todos/` | `getTodos` | List todos |
| `POST /complete_todo/` | `completeTodo` | Mark complete |
| `POST /delete_todo/` | `deleteTodo` | Delete todo |
| `POST /add_reminder/` | `addReminder` | Add reminder |
| `POST /get_reminders/` | `getReminders` | List reminders |
| `POST /delete_reminder/` | `deleteReminder` | Delete reminder |
| `POST /add_calendar_entry/` | `addCalendarEntry` | Add event |
| `POST /get_calendar_entries/` | `getCalendarEntries` | List events |
| `POST /delete_calendar_entry/` | `deleteCalendarEntry` | Delete event |

## Connecting to VAPI
1. Deploy publicly (Railway, Render, or ngrok for local dev)
2. In VAPI dashboard → **Tools** → add a Function tool per endpoint
3. Set the server URL to your deployed endpoint

## Notes
- Dates use ISO 8601 format (`2024-01-15T10:00:00`)
- Swap SQLite for PostgreSQL before deploying at scale
- Add API key auth before exposing endpoints publicly

## License
MIT