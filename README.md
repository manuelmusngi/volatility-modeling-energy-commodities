#### ⚡NYMEX Henry Hub Natural Gas Volatility Modeling  
##### MS‑GARCH • HMM‑GARCH • GARCH vs ML • Hybrid Models

![Python](https://img.shields.io/badge/Python-3.10+-blue.svg)
![License](https://img.shields.io/badge/License-MIT-green.svg)
![Build](https://img.shields.io/badge/Build-Passing-brightgreen.svg)
![Status](https://img.shields.io/badge/Status-Active-success.svg)

---

#### 📌 Overview

This project implements a **research‑grade volatility modeling framework** for the **NYMEX Henry Hub natural gas**, integrating:
- 🔄 **Regime‑Switching Models**  
  ##### MS‑GARCH & HMM‑GARCH (Arouri, Lahiani & Nguyen, 2012)

- 📈 **GARCH‑Family Models**  
  ##### GARCH, EGARCH, FIGARCH

- 🤖 **Machine Learning Benchmarks**  
  ##### Random Forest, XGBoost, LSTM (Chung, 2024)

- 🧠 **Hybrid Models**  
  ##### GARCH‑residual ML correction models

- 🔍 **Full Pipeline**  
  ##### Yahoo Finance data → preprocessing → modeling → forecasting → evaluation → reporting

The goal is to provide a **modular, extensible, and reproducible** platform for volatility forecasting and regime detection in natural gas markets.

---

#### 🧠 Research Foundations

#### **1. Regime‑Switching Volatility**
Arouri, Lahiani & Nguyen (2012) show that natural gas exhibits **distinct volatility regimes**, often linked to structural market events.  

This project implements:

- Hidden Markov Models (HMM)
- Markov‑Switching GARCH (MS‑GARCH)
- Regime‑dependent volatility forecasts
- Smoothed & filtered regime probabilities

#### **2. GARCH vs ML Benchmarking**
Chung (2024) finds:

- Natural gas volatility has **strong persistence**
- Spillovers from other markets are **weak**
- **Hybrid models outperform standalone GARCH or ML**

This project integrates:

- Pure econometric models  
- Pure ML models  
- Hybrid GARCH‑residual ML models  
- Comparative evaluation (MSE, MAE, QLIKE)

---

#### 🧩 Project Architecture

natural-gas-volatility/\
│
├── README.md\
├── [main.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/main.py)\
│
├── config/\
│   ├── [settings.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/config/settings.py)\
│   └── [model_params.yaml](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/config/model_params.yaml)\
│
├── data/\
│   ├── raw/\
│   │   └── henry_hub.csv\
│   │
│   ├── processed/\
│   │   └── returns.csv\
│   │
│   ├── [retrieval.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/data/retrieval.py)\
│   └── [loader.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/data/loader.py)\
│
├── models/\
│   ├── garch/\
│   │   ├── [garch_models.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/models/garch/garch_models.py)\
│   │   └── [ms_garch.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/models/garch/ms_garch.py)\
│   │
│   ├── hmm/\
│   │   └── [hmm_volatility.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/models/hmm/hmm_volatility.py)\
│   │
│   ├── ml/\
│   │   ├── [ml_models.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/models/ml/ml_models.py)\
│   │   └── [hybrid_models.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/models/ml/hybrid_models.py)\
│   │
│   └── [model_factory.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/models/model_factory.py)\
│
├── forecasting/\
│   ├── [rolling_forecast.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/forecasting/rolling_forecast.py)\
│   └── [regime_forecast.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/forecasting/regime_forecast.py)\
│
├── evaluation/\
│   ├── [metrics.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/evaluation/metrics.py)\
│   └── [comparison.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/evaluation/comparison.py)\
│
├── utils/\
│   ├── [logger.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/utils/logger.py)\
│   ├── [plotter.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/utils/plotter.py)\
│   └── [helpers.py](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/utils/helpers.py)\
│
├── reports/\
│   ├── figures/\
│   └── results.csv\
│
└── [requirements.txt](https://github.com/manuelmusngi/volatility-modeling-commodities/blob/main/requirements.txt)


#### License
This project is licensed under the [MIT License](https://github.com/manuelmusngi/regime_switching_models/edit/main/LICENSE).  
