# SentinelPdM

### Offline Predictive Maintenance for Industrial Rotating Equipment

SentinelPdM is an **offline-first predictive maintenance platform** designed to monitor industrial rotating equipment such as pumps, compressors, turbines, motors, and conveyors.

The system uses machine-learning-based failure classification, time-to-failure forecasting, explainable sensor attribution, and rule-based maintenance recommendations — all running **directly inside the browser without a backend, database, or API**.

---

## 🚀 Overview

Unexpected failures in industrial machinery can lead to equipment damage, production downtime, and expensive emergency maintenance.

Traditional approaches such as:

- **Corrective maintenance** — repair equipment after failure
- **Preventive maintenance** — service equipment at fixed intervals

can either result in unnecessary maintenance or fail to detect rapidly developing faults.

**SentinelPdM** takes a predictive approach by continuously analysing equipment telemetry and estimating the probability of failure within the next 24 hours.

The platform can:

- 📊 Monitor multiple industrial assets
- 🤖 Predict failure risk using Machine Learning
- ⏱️ Forecast Time-to-Failure (TTF)
- 🔍 Explain which sensors are contributing to the risk
- 🛠️ Generate maintenance recommendations
- 📁 Analyse real plant telemetry through CSV uploads
- 📄 Generate maintenance reports
- 💬 Provide an offline context-aware assistant
- 🌐 Continue operating without an internet connection

---

## ✨ Key Features

### 🤖 Machine Learning Failure Prediction

SentinelPdM uses **Binary Logistic Regression** to classify whether an asset is likely to fail within the next 24 hours.

The model uses six normalized sensor features:

- Vibration
- Temperature
- Oil Quality
- Motor Current
- Pressure deviation
- RPM deviation

### 📈 Time-to-Failure Forecasting

The system analyses recent risk history and applies a **log-linear exponential trend model** to estimate when the predicted risk will cross a user-defined alert threshold.

Supported forecast horizons:

- 24 hours
- 72 hours
- 168 hours

### 🔍 Explainable AI

Instead of providing only a probability score, SentinelPdM calculates the contribution of every sensor to the current prediction.

For the logistic regression model:

```text
Feature Contribution = Model Weight × Normalized Feature
