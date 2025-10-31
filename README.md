# 🚀 GoQuant REG-NMS Cryptocurrency Matching Engine

A **high-performance cryptocurrency matching engine** inspired by **US SEC Reg-NMS order-matching rules**, built with **Python + Flask**.

Supports **Limit & Market** orders, price-time priority, real-time orderbook, maker-taker fees, and a browser-based trading demo.

---

## ✅ Features

- ⚡ High-performance matching engine
- 📈 Real-time order book (bids/asks)
- 🔄 Limit & Market order support
- 🥇 FIFO (Price-time priority)
- 💰 Maker-Taker fee model
- 🎯 Decimal precision (no float errors)
- 🌐 REST API + UI Demo
- 🧪 Easy local testing

---

## 📁 Project Structure
goquant-reg-nms-matching-engine/
│── src/
│ ├── api/
│ │ └── rest_api.py
│ ├── core/
│ │ ├── matching_engine.py
│ │ ├── order.py
│ │ └── orderbook.py
│── static/
│ └── demo.html
│── requirements.txt
│── run.py
│── README.md

---

## 🛠️ Setup

### 1️⃣ Clone repo
```bash
git clone https://github.com/samprita123/goquant-reg-nms-matching-engine.git
cd goquant-reg-nms-matching-engine

### 2️⃣ Create virtual env
```bash
python -m venv venv

### 3️⃣ Activate env
# Windows
venv\Scripts\activate
# Mac/Linux
source venv/bin/activate

### 4️⃣ Install packages
pip install -r requirements.txt

### 5️⃣ Start server
python run.py

✅ URLs
| URL                            | Use                  |
| ------------------------------ | -------------------- |
| `http://localhost:8000/demo`   | UI trading simulator |
| `http://localhost:8000/health` | Health check API     |

📡 API
### ▶️ Submit Order

POST /api/v1/order
{
  "symbol": "BTCUSDT",
  "order_type": "limit",
  "side": "buy",
  "price": "35000",
  "quantity": "0.5"
}


### 📖 Orderbook

GET /api/v1/orderbook/BTCUSDT

### 🔧 Test with curl
curl -X POST "http://localhost:8000/api/v1/order" \
-H "Content-Type: application/json" \
-d '{"symbol":"BTCUSDT","order_type":"limit","side":"buy","price":"35000","quantity":"1"}'


### 🧭 Roadmap

✅ Core matching engine

✅ REST API + demo UI

🔜 WebSocket live stream

🔜 Persistent DB (Postgres/Redis)

🔜 Advanced trading dashboard

🔜 Docker deployment

👩‍💻 Author

Samprita Patra
High-performance systems | ML | Web Dev

⭐ If this project helped you, please star the repo!
