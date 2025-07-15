
# 🎬 Streaming Service Engagement Analytics & Growth Experiments

## 🔍 Project Overview (📘 [Click here to view the full Colab notebook](https://github.com/NihalMat/streaming-engagement-analytics/blob/main/Streaming_Analytics_Colab.ipynb))
This project simulates a real-world analytics case study for a digital streaming platform (Netflix, Prime, Apple Tv+)  
We focus on understanding user behavior, uncovering growth levers, and validating product strategies with data.

**Key Goals:**
- Understand how early user behavior (genre diversity, session patterns) affects retention.
- Simulate A/B tests to validate product ideas (e.g., push notifications).
- Translate raw metrics into business outcomes like revenue impact or session uplift.
- Communicate findings in actionable, stakeholder-friendly formats.

---

## 🧱 Dataset Simulation
We created a synthetic dataset mimicking a streaming platform:
- `users.csv` → user_id, platform, country, signup timestamp
- `content.csv` → content_id, genre, duration, release date
- `events.csv` → user_id, content_id, event_type (play, pause, skip), timestamp

We joined and transformed these into a unified `fact_streaming_activity` table using Spark (Databricks initially, then migrated to Colab).

---

## 📈 Part 1: Retention Metrics

### 🎯 Goal: Understand D1, D7, D30 retention

We defined **retention** as users who returned to watch content on Day 1, 7, or 30 post-signup.

| Metric             | Value     |
|--------------------|-----------|
| D1 Retention Rate  | 8.0%      |
| D7 Retention Rate  | 8.3%      |
| D30 Retention Rate | 8.4%      |

📉 **Insight**: The initial retention rates are low. We need to investigate product factors.

---

## 🎭 Part 2: Behavior-Based Segmentation

### 🔄 Genre Diversity → Retention
We computed how many genres users explored in their first 3 days and correlated that with D7 retention.

| #Genres Explored | D7 Retention |
|------------------|--------------|
| 1                | 6.4%         |
| 2                | 8.1%         |
| 3                | 10.3%        |
| ≥4               | **12.4%**    |

📌 **Insight**: Users exploring more genres retained better. Content discovery drives stickiness.

---

## 📲 Part 3: A/B Testing – Push Notifications

### 🧪 Hypothesis:
> Sending daily push notifications after signup increases average session frequency in the first 7 days.

| Group | Treatment                      | Avg. Sessions (7D) |
|-------|--------------------------------|--------------------|
| A     | No notifications (Control)     | 49.9               |
| B     | Daily push reminders (Variant) | **59.8**           |

- 🔬 T-Test: **p < 0.001**
- 📊 95% CI: Sessions increased with high confidence

📈 **Outcome**: Modeled **~10 extra sessions per user** globally if this were rolled out.

---

## 🔍 Strategic Takeaways

### 🧠 Product Insights:
- Users who discover more genres are more likely to return → improve homepage recommendations.
- Timely nudges (push notifications) drive habit formation → automate onboarding reminders.

### 📊 Metrics That Matter:
- D7 Retention by behavior
- Session uplift through A/B testing
- Genre diversity as a leading indicator

### 💼 Value Delivered:
- Identified key levers to improve retention by up to **4.2 percentage points**
- Simulated impact of global rollout: **millions of additional sessions**
- Built reusable analytics framework with product-aligned experimentation

---

## 🔧 Tools & Skills Used
- **Python (Pandas, Seaborn, Matplotlib)**
- **A/B Testing (Z-test, T-test)**
- **Data Cleaning & Transformation**
- **Product Metrics Design**
- **Colab + Databricks (migrated)**

---

## 📣 Summary

This project demonstrates how an analytics team can:
- Go from raw events → retention metrics → product experiments
- Back hypotheses with **statistical tests**
- Convert insights into **business action**
- Communicate findings in a format executives can act on

It reflects a **real-world analytics loop** — from metric definition to product iteration to ROI modeling.
