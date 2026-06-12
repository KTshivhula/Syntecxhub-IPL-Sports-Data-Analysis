# 🏏 IPL Sports Data Analysis

**Complete analytics pipeline for IPL (Indian Premier League) data (2008–2024)**  
Author: Khoro Avhavhoni Tshivhula  
Date: 2026-06-12

---

## 📌 Project Overview

This project performs end-to-end analysis of IPL cricket data, including:

- **Descriptive Analytics** – Top batsmen, bowlers, team win rates, venue scoring patterns
- **Diagnostic Analytics** – Home advantage, toss impact by venue, player consistency across seasons
- **Predictive Analytics** – Match winner prediction using Logistic Regression, Random Forest, and XGBoost
- **Unsupervised Learning** – Player clustering (K‑Means + Hierarchical) to identify Power Hitters, Anchors, All‑Rounders, and Bowlers

All results are exported as charts and summary reports, ready for stakeholders (team management, fantasy sports platforms, broadcasters).

---

## 📂 Project Structure

IPL Sports Data Analysis/
├── Data/
├── Notebook/
├── Charts/
├── Reports/
├── requirements.txt
└── README.md


---

## 🚀 Key Results

### 🔥 Batting
| Category | Leader | Value |
|----------|--------|-------|
| Most runs | Virat Kohli | 7,995 |
| Highest strike rate (min 100 balls) | Jake Fraser‑McGuirk | 238.2 |
| Most sixes | Chris Gayle | 354 |
| Most fours | Shikhar Dhawan | 763 |

### 🎯 Bowling
| Category | Leader | Value |
|----------|--------|-------|
| Most wickets | Yuzvendra Chahal | 213 |
| Best economy (min 20 overs) | Sohail Tanvir | 6.23 |

### 🏆 Teams
| Team | Total Wins |
|------|-------------|
| Mumbai Indians | 144 |
| Chennai Super Kings | 138 |
| Kolkata Knight Riders | 131 |

### 🎲 Toss Impact
- Toss winner wins only **49.4%** of matches – toss is **not decisive**.

### 🏟️ Venue Insights
| Most Batting‑Friendly (runs/wicket) | Most Bowling‑Friendly (runs/wicket) |
|--------------------------------------|--------------------------------------|
| Mohali (33.4) | Kingsmead, Durban (21.7) |
| Hyderabad (32.9) | Dr DY Patil, Mumbai (22.3) |
| Jaipur (32.6) | Chepauk, Chennai (24.8) |

### 👥 Player Clustering (K‑Means, k=4)

| Cluster | Role | Examples |
|---------|------|----------|
| 0 | Power Hitter | A Russell, K Pollard, G Maxwell |
| 1 | Anchor | V Kohli, S Dhawan, RG Sharma |
| 2 | All‑Rounder | H Pandya, R Jadeja, S Watson |
| 3 | Bowler | J Bumrah, Y Chahal, Rashid Khan |

> Only **63 genuine all‑rounders** exist in IPL history (min 200 balls + 300 deliveries).

---

## 📈 Predictive Modeling

We built three models to predict match winners using pre‑match features (teams, venue, toss, season).

| Model | Test Accuracy | F1 Score | 5‑Fold CV Accuracy |
|-------|---------------|----------|---------------------|
| Logistic Regression | 22.9% | 0.192 | 17.6% |
| Random Forest | 46.3% | 0.451 | 38.7% |
| **XGBoost (best)** | **48.6%** | **0.475** | 34.9% |

**Key insight:** Predicting IPL winners is very hard – even the best model barely outperforms random guessing (5.3% baseline). Team identity is the strongest feature, while toss contributes only ~21%.

---

## 🛠️ Requirements & Setup

### Dependencies
Install the required Python libraries:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost scipy
