# 🥷 Backpack2 安全版 刷分專用機器人

專為 Backpack 交易所設計的自動化交易與刷分腳本。

> 目標：高效刷分 ✅ 低風險 ✅ 減少風控 ✅

---

## ✨ 功能簡介
- 自動掛單 + 自動吃單
- 安全分倉控制
- 自動止損機制
- 成交數據記錄
- 支援 USDC / SOL 兩邊交易
- 完整自訂參數（API、區間、網格、倉位等）

---

## ⚙️ 基本結構
```
backpack2-safe/
├── README.md              # 說明文件
├── config.py               # 參數設定檔
└── backpack2_safe_bot.py   # 主程式（安全版刷分機器人）
```

---

## 🔧 配置教學

### Step1. 編輯 `config.py`

使用 VPS 內指令：
```bash
nano config.py
```

修改以下內容（替換為你的資訊）：
```python
API_KEY = 'YOUR_API_KEY'
API_SECRET = 'YOUR_API_SECRET'
SYMBOL = 'SOL_USDC'
GRID_LOWER_PRICE = Decimal('122.68')
GRID_UPPER_PRICE = Decimal('129.41')
GRID_NUM = 20
GRID_INVESTMENT = 200
STOP_LOSS_PERCENT = 7
MONITOR_INTERVAL_SECONDS = 60
```

---

## 🚦 啟動方式

```bash
python3 backpack2_safe_bot.py
```

---

## 📊 成交紀錄
每筆成交將自動輸出如下格式：
```
[成交] 第 1 筆 | BUY | 價格: 126.50 | 數量: 0.05 | 手續費: 0.03 | 累計盈虧: -6.33
```

---

## 🟣 注意事項
- 適合長時間掛單刷分
- 請嚴格控制倉位與止損百分比
- 建議配合多帳號、分倉操作
- API 請勿外洩
- 本腳本僅供學術研究，請自行承擔使用風險

---

© ShadowEdge for Sky 專屬定制

