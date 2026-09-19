# Netflix User Behavior Analysis

Exploratory analysis of Netflix subscriber behavior — subscription plans, revenue, device usage, geography, and account activity.

**SkillInfyTech Data Science Internship — Project 3**

---

## Overview

What can user data tell us about viewer preferences and trends on Netflix? This project analyzes a Netflix userbase dataset to uncover patterns in subscription choices, revenue distribution, device usage, and demographic trends — the kind of analysis a streaming platform's growth or retention team would run to understand its subscriber base.

**Dataset:** Netflix Userbase Dataset (Kaggle, 2,500 users) — subscription type, monthly revenue, join/payment dates, country, age, gender, device, and plan duration.

---

## Tech Stack

- **Data processing:** Pandas, NumPy
- **Visualization:** Matplotlib, Seaborn

---

## Key Findings

- **Most popular plan:** Basic leads with 999 users (~40%), followed by Standard (768) and Premium (733) — a fairly even three-way split skewed toward the cheapest tier
- **Revenue is plan-driven, not demographic-driven:** Average monthly revenue is nearly flat across all 10 countries (~$12-13), and correlation analysis shows no meaningful relationship between Age and Monthly Revenue
- **No dominant device:** Usage is split almost evenly across Laptop (25.4%), Tablet (25.3%), Smartphone (24.8%), and Smart TV (24.4%) — users aren't converging on a single platform
- **Gender is balanced within every tier:** Male/Female counts are nearly identical across Basic, Standard, and Premium subscribers
- **Age spans 26-51** fairly evenly, with mild peaks around 31, 36, 41, and 46 — no single dominant age segment
- **Dataset limitation:** every user is on a "1 Month" plan duration, so this dataset can't be used to study long-term commitment or churn by contract length

---

## Correlation Analysis

A correlation heatmap across the numeric features (User ID, Monthly Revenue, Age) showed no meaningful linear relationships — revenue is determined entirely by which subscription tier a user picks, not by their age or any other numeric attribute in this dataset.

---

## Business Takeaway

Because device usage, revenue, and demographics are all nearly uniform across the userbase, there's no obvious "high-value" segment to target based on this data alone. Retention and upsell efforts would be better aimed at **subscription tier movement** — converting Basic users to Standard or Premium — rather than targeting by device, country, or age group. The near-even device split also suggests the platform experience needs to stay consistent across all four device types, since no single device dominates usage.

---

## Project Structure

```
netflix-user-behavior/
├── data/                          # Dataset (gitignored)
├── notebooks/
│   └── netflix_analysis.ipynb     # Full EDA pipeline
├── requirements.txt
└── README.md
```

---

## Run Locally

```bash
git clone https://github.com/Vinisha-Victor/netflix-user-behaviour.git
cd netflix-user-behavior

python -m venv .venv
.venv\Scripts\Activate.ps1      # Windows
pip install -r requirements.txt

jupyter notebook notebooks/netflix_analysis.ipynb
```