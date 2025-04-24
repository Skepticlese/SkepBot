# SkepBot

A feature-rich Discord bot offering a virtual economy, mini‑games, custom commands, and session tracking.

---

## 🚀 Features

- **Economy System**: Persistent coin balances per user.  
- **Mini‑Games**:  
  - Slots  
  - Blackjack  
  - Weekly Lottery (capped tickets per user, centralized pot)  
- **Custom Commands**: Server‑specific dynamic `!commands` configurable at runtime.  
- **Session Tracking**: Track wins/losses, display live scoreboards, and update or move scoreboard messages on demand.  
- **Configurable & Modular**: Built with Cogs and utility modules for easy extension.

---

## 📦 Installation

1. **Clone the repo**
   ```bash
   git clone https://github.com/Skepticlese/SkepBot.git
   cd SkepBot
   ```
2. **Create a virtual environment** (recommended)
   ```bash
   python -m venv venv
   source venv/bin/activate   # macOS/Linux
   venv\Scripts\activate    # Windows
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```
4. **Configure environment**
   - Copy `.env.example` to `.env` and fill in your Discord bot token and other settings.

---

## ⚙️ Configuration

- **`.env` variables**:  
  ```ini
  DISCORD_TOKEN=your-bot-token
  PREFIX=!                # Command prefix
  LOTTERY_DAY=Monday       # Day for weekly lottery draw
  LOTTERY_TIME=18:00       # 24h time (server timezone)
  ```
- **JSON state files**:
  - `commands.json`: Stores custom commands per guild.  
  - `lottery_state.json`: Tracks entries and pot amount.

---

## 📝 Usage

- **Economy**  
  - `!balance` — Show your current coin balance.  
  - `!give @user <amount>` — Transfer coins to another user.

- **Slots & Blackjack**  
  - `!slots <bet>`  
  - `!blackjack <bet>`

- **Lottery**  
  - `!buytickets <n>` — Purchase up to 150 tickets.  
  - Lottery draw runs automatically per schedule.  

- **Custom Commands**  
  - `!addcmd <name> <response>` — Create a new command.  
  - `!delcmd <name>` — Remove a custom command.

- **Session Scoreboards**  
  - `!start_session` — Begin a new session.  
  - `!win` / `!lose` — Record a result and update the scoreboard.  
  - `!stop_session` — End session and post final standings.

---

## 📂 Folder Structure

```
SkepBot/
├── cogs/                  # Bot functionality modules
├── utils/                 # Helper functions (e.g., data persistence)
├── data/                  # JSON state files
├── requirements.txt       # Python dependencies
├── .env.example           # Sample environment variables
└── bot.py                 # Entry point
```

---

## 🤝 Contributing

1. Fork the repository.  
2. Create a feature branch: `git checkout -b feature/YourFeature`  
3. Commit changes: `git commit -m "Add YourFeature"`  
4. Push to branch: `git push origin feature/YourFeature`  
5. Open a Pull Request.

Please follow the existing code style and include tests where appropriate.

---

## 📝 License

This project is licensed under the [MIT License](LICENSE).

---

## 📄 Terms of Service

Your bot’s Terms of Service are maintained in a separate document:
- [Terms of Service](./TERMS_OF_SERVICE.md)

