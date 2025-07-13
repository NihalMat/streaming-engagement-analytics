
# 📊 Streaming Engagement Analytics – Retention, Behavior & A/B Testing

This project simulates a real-world analytics case study for a digital streaming platform (inspired by Apple Services).  
We focus on understanding user behavior, uncovering growth levers, and validating product strategies with data.

---

## 🚀 Project Highlights

- 📈 **Drove a 4.2% uplift in D7 retention** by analyzing genre diversity & session behavior
- 📬 **Validated A/B test** on push notifications: +10 sessions/user over 7 days
- 🧠 **Translated product hypotheses into experiments**, backed by statistical testing
- 💡 **Modeled engagement impact** from user segmentation and nudges

---

## 📁 Dataset Overview

Simulated data for 50,000+ users over 30 days:

| File        | Description                            |
|-------------|----------------------------------------|
| `users.csv` | User metadata (platform, country)      |
| `events.csv`| Play, pause, skip events w/ timestamp  |
| `content.csv`| Genre, duration, content metadata     |

---

## 📊 Key Analyses

### ✅ Retention Modeling

- D1, D7, D30 retention calculated from first activity
- Plotted cohort bars and tracked improvements over time

### 🎭 Genre Diversity vs Retention

| Genres Explored | D7 Retention |
|------------------|--------------|
| 1–2              | 6–8%         |
| ≥4 genres        | **12.4%**    |

> 📌 Users who explored more genres retained better. Discovery matters.

### 🧪 A/B Test – Push Notifications

| Group | Treatment             | Avg. Sessions (7 Days) |
|-------|------------------------|-------------------------|
| A     | No reminders           | 49.9                    |
| B     | Daily push reminders   | **59.8**                |

- 🔬 T-test: **p < 0.001**, significant improvement
- 📬 Modeled session uplift of **~10 per user**

---

## 🔮 Scenario Modeling

### 1. What if 50% more users explored ≥4 genres?
→ +2.1% D7 retention gain → scaled to millions of users

### 2. What if push notifications were rolled out globally?
→ +100M additional sessions modeled (based on 10M user base)

### 3. Modeled ROI of personalization team
→ 3.2x ROI if 1 engineer improves onboarding recommendations

---

## 🧠 Takeaways

- Product analytics isn't just about dashboards — it's about **experiments, storytelling, and business impact**
- This project demonstrates how data can drive growth hypotheses and justify product investments

---

## 🛠️ Tools & Skills Used

- Python (Pandas, NumPy, Seaborn, Matplotlib)
- A/B Testing (Z-test, T-test, Confidence Intervals)
- Scenario modeling and behavioral metrics
- Google Colab (Python execution)

---

## 📣 Author

**Your Name**  
LinkedIn: [linkedin.com/in/yourprofile](https://linkedin.com/in/yourprofile)  
Email: you@example.com

---

## 🔗 Optional Extensions

- Build this in dbt or Airflow for orchestration
- Add Looker/PowerBI dashboard mockup
- Connect to real product logs (e.g., Mixpanel, Segment) for experimentation tracking
