# 🧠 Reinforcement Learning for Portfolio Optimization

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TarunReddy77/Reinforcement-Learning-based-Portfolio-Optimization/blob/main/Porfolio_Optimization_using_Reinforcement_Learning.ipynb)

This project explores how Reinforcement Learning (RL) can be applied to optimize portfolio value through intelligent trading decisions. We model trading as a sequential decision-making problem and implement several RL algorithms to train agents that buy, sell, or hold based on market context.

---

## 📌 Problem Statement

Traditional trading systems often fail to:
- Capture **sequential dependencies**
- Adapt to **non-stationary** financial markets

Reinforcement Learning offers a natural fit for trading, aligning with its core loop:
> State → Action → Reward → Policy Update

The goal is to **maximize long-term cumulative return** by learning policies that evolve through experience.

---

## 🗃️ Dataset & Features

- **Source**: Yahoo Finance (`yfinance` API)
- **Ticker**: AAPL (Apple Inc.)
- **Period**: 2010–2024
- **Granularity**: Daily OHLCV data

### Engineered Features:
- 📈 Price Change %, Daily Range %
- 📉 SMA_5, SMA_50, EMA_10
- 🔁 ATR, RSI

> ✂️ Split: 80% training | 20% testing

---

## 🏗️ Custom Gym Environment

A custom [OpenAI Gym](https://www.gymlibrary.dev/) environment was built to simulate real-world trading using daily market data.

- **State**: Vector of 7 engineered features  
- **Action Space**:  
  - 0: Hold  
  - 1: Buy (if cash available)  
  - 2: Sell (if stock owned)  
- **Reward**: Change in portfolio value  
- **Termination**: End of dataset

---

## 🧠 RL Algorithms Compared

We evaluated multiple agents:

| Agent           | Type                 |
|----------------|----------------------|
| Random Agent   | Baseline             |
| Q-Learning     | Tabular              |
| DQN            | Deep Q-Network       |
| Rainbow DQN    | Ensemble + Priority  |
| PPO            | Policy Gradient      |
| A2C            | Advantage Actor-Critic |

---

## 📊 Evaluation Metrics

- **Total Return**
- **Sharpe Ratio**
- **Max Drawdown**
- **Volatility**

---

## 📈 Results

- **Rainbow DQN** and **PPO** outperformed others in terms of return and Sharpe ratio.
- Traditional methods (Q-learning) struggled with long-term optimization.
- Advanced RL agents learned to minimize drawdowns while maximizing gains.

---

## 🚀 Running the Notebook

> ⚠️ Notebook is large and may not render on GitHub — open in Colab for best experience:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/TarunReddy77/Reinforcement-Learning-based-Portfolio-Optimization/blob/main/Porfolio_Optimization_using_Reinforcement_Learning.ipynb)

---

## 🧩 Future Work

- Multi-asset portfolio optimization
- Incorporating news sentiment and macroeconomic indicators
- Live trading integration using broker APIs

---

## 📎 Project Author

**Tarun Reddy Thandu**  
Master’s in Artificial Intelligence  
Northeastern University, Boston  
[LinkedIn](https://www.linkedin.com/in/tarun-reddy) | [Portfolio](https://tarunreddy77.github.io/portfolio)

