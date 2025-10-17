# Python Trading Bot — Bert 🐍📈

A complete trading bot starter built **entirely from scratch in Python**, featuring:

* Paper trading simulation
* MA Crossover strategy
* Simple backtester
* SQLite trade logging
* Flask web dashboard (real-time trade view)

This is **educational**, clean, and easy to extend into a **fully automated trading system** connected to live brokers (Zerodha, Binance, etc.).

---

## ⚙️ Features

* 🧠 **Modular structure** — broker, strategy, risk, and execution are separated for easy modification.
* 💰 **Paper Broker** — simulate trades and balances before going live.
* 🧾 **MA Crossover Strategy** — basic signal generator (can be swapped for custom logic or ML models).
* 🧮 **SQLite Logging** — all trades stored locally.
* 🌐 **Web Dashboard (Flask)** — see trade history and bot status instantly.
* 🔍 **Backtester** — test strategies with dummy or historical data.
* 🧰 **CLI Tools** — start/stop bot and view logs quickly.

---

## 🧩 Project Structure

```
trading-bot/
├─ config/
│  └─ config.yml
├─ requirements.txt
├─ README.md
└─ src/
   ├─ broker.py
   ├─ strategy.py
   ├─ risk.py
   ├─ db.py
   ├─ executor.py
   ├─ backtest.py
   ├─ webapp.py
   └─ cli.py
```

---

## 🚀 Getting Started

```bash
# 1. Clone this repo
git clone https://github.com/your-username/python-trading-bot.git
cd python-trading-bot

# 2. Install dependencies
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt

# 3. Initialize the database
python3 -c "from src.db import init_db; init_db()"

# 4. Run the bot (paper mode)
python3 src/executor.py

# 5. Run web dashboard
python3 src/webapp.py
```

Visit **[http://localhost:5000/api/status](http://localhost:5000/api/status)** or **/api/trades** to see the live status.

---

## 🧠 Strategy

The included **MA crossover** strategy generates BUY when fast MA crosses above slow MA, and SELL when it crosses below.

```python
signal = ma_crossover_signal(df, fast=9, slow=21)
```

Replace this with your own custom indicator, sentiment model, or ML strategy.

---

## 💡 Next Steps

* Integrate **Kite Connect** or **Binance API** for live trading.
* Add **stop-loss / take-profit** management.
* Use **backtrader** or **vectorbt** for advanced backtesting.
* Add **Telegram alerts** and risk control dashboards.

---

## ⚠️ Disclaimer

This bot is for **educational purposes only**. Use at your own risk. The author assumes **no responsibility for financial losses**.

---

## 📄 License

OpenSource License — free to use, modify, and share.

---

💬 **Contributions welcome!**
If you improve it (add brokers, indicators, or UI), feel free to open a pull request.

Releasing on 12th March 2026 for public use
