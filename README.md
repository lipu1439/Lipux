# Vercel Flask Verification App with Telegram Bot

This project contains:
- **app.py**: A Flask application deployed on Vercel that handles `/verify/<code>` verification.
- **vercel.json**: Vercel configuration for the deployment.
- **requirements.txt**: Python dependencies for Vercel and bot.
- **.env.example**: Sample environment variables configuration.
- **bot.py**: (Optional) Telegram bot code to handle user requests (must be deployed on another platform).

## Deployment Instructions

### Vercel (for Flask App)
1. Clone this repository.
2. Create a `.env` file in the root directory using `.env.example` as reference.
3. Install [Vercel CLI](https://vercel.com/docs/cli) and deploy:
   ```bash
   vercel login
   vercel
   ```

### Telegram Bot
- Deploy `bot.py` on a separate platform (e.g., Railway, Fly.io, Heroku).
- Configure the `.env` with valid environment variables.

## Folder Structure
```
/your-repo
├── app.py
├── vercel.json
├── requirements.txt
├── .env.example
├── bot.py         # Optional
└── README.md
```

## Important Notes
- Do NOT upload your real `.env` to GitHub. Keep sensitive credentials safe.
- The bot and Flask app work together, but Vercel cannot host the long-running bot process.