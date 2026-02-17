<p align="center">
  <img src="https://img.shields.io/badge/Ludo-Hub-blueviolet?style=for-the-badge&logo=telegram" alt="LudoHub"/>
</p>

<h1 align="center">🎲 LudoHub</h1>

<p align="center">
  <b>A Real-Time Multiplayer Ludo Game with Telegram Bot Integration</b>
</p>

<p align="center">
  <a href="#features"><img src="https://img.shields.io/badge/Features-⭐-gold?style=flat-square" alt="Features"/></a>
  <a href="#deployment"><img src="https://img.shields.io/badge/Deploy-VPS-green?style=flat-square" alt="Deploy"/></a>
</p>

---

## 📖 About
**LudoHub** is a real-time multiplayer Ludo game integrating Telegram. Play with friends, chat in-game, and enjoy smooth animations.

---

## 🚀 VPS Deployment (Simple & Fast)

Run these commands one by one to deploy on your VPS (Ubuntu/Debian).

### 1. Update & Install Requirements
```bash
sudo apt update
sudo apt install -y python3-pip python3-venv git nodejs nano
sudo npm install -g pm2
```

### 2. Clone Repository
```bash
git clone https://github.com/yourusername/LudoHub.git
cd LudoHub
```

### 3. Setup Python Environment
```bash
python3 -m venv venv
source venv/bin/activate
pip install "pymongo<4.0" motor
pip install -r requirements.txt
```

### 4. Configure Settings
```bash
cp .env.example .env
nano .env
```
*Edit the file with your API keys, then save (Ctrl+X, Y, Enter).*

### 5. Run the Bot
```bash
pm2 start "venv/bin/python3 -m LudoHub" --name ludo
pm2 save
pm2 startup
```

**That's it! Your bot is now online.** 🚀

---

### Useful Commands
- **Check Status:** `pm2 status`
- **View Logs:** `pm2 logs ludo`
- **Restart:** `pm2 restart ludo`
- **Stop:** `pm2 stop ludo`

---

## 💻 Local Run
```bash
git clone https://github.com/yourusername/LudoHub.git
cd LudoHub
python -m venv venv
# Windows: venv\Scripts\activate | Linux: source venv/bin/activate
pip install -r requirements.txt
# Configure .env
python -m LudoHub
```

---

## 📁 Project Structure
```
LudoHub/
├── LudoHub/            # Main Source Code
│   ├── bot/            # Telegram Bot Plugins
│   ├── core/           # Game Logic & Database
│   ├── web/            # FastAPI & Socket.IO
│   ├── static/         # Frontend (HTML/CSS/JS)
│   └── assets/         # Audio Files
├── .env                # Config Keys
└── requirements.txt    # Dependencies
```

---

## 📄 License
This project is licensed under the MIT License.
