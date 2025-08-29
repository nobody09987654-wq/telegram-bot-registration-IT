# ITeach Academy Registration Bot

A Telegram bot for course registration, designed for easy deployment on [Railway](https://railway.app/).

## Features

- Multi-step user registration for courses
- Admin notification
- PostgreSQL-backed data storage

## Quickstart

### 1. Clone repo
```bash
git clone https://github.com/YOUR_USERNAME/telegram-bot-registration.git
cd telegram-bot-registration
```

### 2. Set up Railway

- Create a new project on Railway.
- Add environment variables in the Railway dashboard:
    - `BOT_TOKEN` — Telegram bot token
    - `ADMIN_ID` — Your Telegram user ID
    - `DATABASE_URL` — Railway provides this automatically if you add a PostgreSQL plugin

### 3. Deploy

Railway will auto-detect your `Procfile` and `requirements.txt` and deploy your bot.

### 4. Local testing

If you want to run locally, create a `.env` file with the same variables:
```
BOT_TOKEN=xxxx
ADMIN_ID=123456
DATABASE_URL=postgresql://...
```
Then, use [`python-dotenv`](https://pypi.org/project/python-dotenv/) to load `.env` before your imports in `Main.py`:
```python
from dotenv import load_dotenv
load_dotenv()
```

## License

MIT