# Berkeley Engineering AI/ML
Apply exploratory data analysis, plotting, statistical summarization, and data visualization skills and techniques to a machine learning problem.

# 🚗 Coupon Acceptance Analysis – Bar vs Other Offers

## 📋 Overview

This project analyzes customer behavior when offered location-based driving coupons for places like bars, coffee shops, and restaurants. The goal is to identify the key factors that influence whether a customer **accepts** a coupon or not, focusing specifically on **bar coupons** and **passenger-related behavior**.

Data was sourced from the UCI Machine Learning Repository and includes simulated driving scenarios collected via Mechanical Turk.

---

## 📁 Dataset

- `coupon_data.csv`: Includes driver demographics, trip context (destination, weather, passenger type), and whether the coupon was accepted.
- Each row represents a driver's response to a specific coupon offer in a unique driving context.

---

## 🎯 Objectives

1. Explore general coupon acceptance patterns.
2. Focus on **bar coupon acceptance** and compare it across:
   - Bar visit frequency
   - Passenger type
   - Age groups
   - Occupation and marital status
3. Extend analysis to other coupon types (e.g., Coffee House) for independent investigation.
4. Test custom group hypotheses using compound filters.
5. Visualize relationships between variables and acceptance outcomes.

---

## 🛠 Key Methods

- Cleaned missing values using `dropna()`.
- Converted categorical ranges (e.g., `'1~3'`) to numeric using mapping dictionaries.
- Created derived numeric columns like:
  - `bar_freq_num`
  - `restaurant20_freq_num`
  - `age_num` (from string ranges)
- Filtered groups using logical conditions for custom hypotheses.
- Used bar plots, histograms, and count plots with `matplotlib` and `seaborn` for visualization.

---

## 📊 Insights

- Drivers who visit bars **more than once a month**, are **under 30**, and **aren’t driving with kids** are more likely to accept bar coupons.
- Social context (e.g., driving with friends or a partner) increases acceptance rate.
- Younger drivers and those with **lower income and frequent restaurant visits** tend to accept **Coffee House** coupons more often.
- Mapped compound hypotheses revealed that targeting **active, younger, social drivers** yields higher coupon acceptance.

---

## 📦 Libraries Used

- `pandas`
- `numpy`
- `matplotlib`
- `seaborn`
- `re` (for text extraction)
- `sklearn` (optional for modeling)

---

## 📁 File Structure

