# Black Gold – Telegram War Strategy Bot

🇮🇷👑 **Designed for Persian-speaking users** – All menus, messages, and commands are in Farsi (Persian).

⚔️ **A complete geopolitical strategy game inside Telegram**  
Manage your country, build your army, trade oil and weapons, declare official statements, and attack other nations – all from your Telegram chat.

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![Telegram Bot API](https://img.shields.io/badge/Telegram%20Bot%20API-7.0+-blue.svg)
![SQLite](https://img.shields.io/badge/SQLite-3-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 🌍 Overview

**Black Gold** is a full-featured Telegram bot that simulates a global war scenario. Each player chooses a country or a paramilitary group and acts as its commander. You must manage your economy, purchase military equipment, buy international companies, trade with other nations, publish official declarations, and launch military attacks — all in real time.

---

## 🚀 Features

### 🏛️ Country & Group Selection
- Choose from **80+ real countries** (with flags, oil resources, VIP status)
- Or pick a **paramilitary group** (Hamas, Mossad, Anonymous, etc.)
- Each country has unique traits: oil-rich, VIP access to special weapons

### 💰 Economy & Daily Income
- Every day at midnight, all players receive their **daily income**
- Oil-producing countries earn **oil reserves** daily
- Companies generate **passive income** and **produce equipment** automatically
- Purchase **mines** to earn additional daily revenue

### 🛒 Weapons Shop
8 categories of military equipment:
- 🔫 Ground Forces (soldiers, commanders, spies, snipers, RPGs, etc.)
- ✈️ Air Force (F-16, F-22, F-35, B-2 bombers, etc.)
- ⚓ Navy (oil tankers, submarines, aircraft carriers, warships)
- 🚀 Missiles (precision, cruise, Khorramshahr, DF-26, atomic bomb)
- 🛬 Drones (suicide, precision, reconnaissance)
- 🚁 Helicopters (Apache, Cobra, Crocodile)
- 🛡️ Defense (Patriot, Phalanx, THAAD)
- 🚜 Tanks (Zolfaghar, Panther, Karrar)

### 🏢 International Companies
Buy companies to boost your economy and automate equipment production:
- Aircraft factory, tank factory, drone factory, missile factory
- Naval shipyard, helicopter manufacturer, defense systems
- Hack company, energy company, intelligence agency
- Each company produces a fixed number of units daily

### 📦 International Trade
- Export weapons and oil to other countries
- Set your own price (or offer for free)
- Trade requests are sent directly to the target player
- 15-minute delivery animation after acceptance

### 📢 Official Declarations
- Write official political statements
- Submitted to admin for approval
- Approved declarations are published in the main group and channel
- Rejected declarations are notified to the player

### 💣 Military Attack System
- Choose a target country (except your own)
- **Weekly attack limit**: You can attack a specific country only once per week
- **Retaliation allowed**: If a country attacks you, you may attack them back even if you already attacked them that week
- Choose attack type: Air, Ground, Missile, Drone, or Armored
- Select units and quantity based on your inventory
- Attack power vs. defense power calculation
- Success probability based on power ratio (with randomness)
- Results: budget loss, satisfaction loss, equipment destruction for defender; loot and casualties for attacker
- Public announcement in the main group
- Private notification to both attacker and defender

### 🏆 Ranking System
- Points calculated from:
  - Budget (×1.0)
  - Successful attacks (×5.0)
  - Total attacks (×2.0)
  - Total equipment (×0.5 per 100 units)
  - Popular satisfaction (×0.2 per 100%)
- Top 10 players displayed with medals
- Your own rank and detailed stats shown

### 👑 Admin Panel
- Manual income distribution to all players
- Declaration approval/rejection
- Full control over the game state

---

## 🛠️ Technologies

- **Python 3.10+**
- **python-telegram-bot** (v20.7) with JobQueue support
- **SQLite3** (lightweight embedded database)
- **asyncio** for asynchronous operations

---

## 📦 Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/black-gold-bot.git
cd black-gold-bot
```

2. Create a virtual environment (optional but recommended)
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies
```bash
pip install "python-telegram-bot[job-queue]==20.7"
# Optional: install pytz if you need timezone support
pip install pytz
```

4. Configure the bot
Edit bot.py and set your:

```python
TOKEN = "YOUR_BOT_TOKEN"           # from BotFather
ADMIN_ID = YOUR_TELEGRAM_USER_ID   # your numeric user ID
GROUP_1_ID = -1001234567890        # group ID for public announcements
CHANNEL_ID = -1001234567890        # channel ID for declarations
REQUIRED_CHANNELS = ["@Channel1", "@Channel2"]  # channels users must join
```

5. Run the bot
```bash
python bot.py
```
