# 🏋️‍♂️ Aerofit Business Case Study

## 📘 Project Overview
**Topic:** Exploratory Data Analysis (EDA)  

Aerofit is a leading brand in the field of fitness equipment, offering a wide range of products such as treadmills, exercise bikes, gym equipment, and fitness accessories.  
The purpose of this project is to analyze customer data and identify **key characteristics of the target audience** for each treadmill model — **KP281, KP481, and KP781**.

This analysis helps Aerofit provide **better product recommendations**, understand **customer behavior**, and develop **data-driven marketing strategies**.

---

## 🎯 Case Objectives

### From the Company’s Perspective
- Identify target audience characteristics for each treadmill.
- Perform **descriptive analytics** to build customer profiles.
- Construct **two-way contingency tables** and compute **conditional and marginal probabilities**.
- Use these insights to improve marketing and sales recommendations.

### From the Learner’s Perspective
- Gain hands-on experience in **data analysis and visualization**.
- Understand how to interpret relationships between input and output variables.
- Develop practical analytical skills relevant to real-world business contexts.

---

## 🧩 Dataset Information

**Dataset:** `aerofit_treadmill_1`

| Column | Description |
|:---------|:-------------|
| `Product` | Product purchased (KP281, KP481, KP781) |
| `Age` | Customer age (in years) |
| `Gender` | Male / Female |
| `Education` | Education (in years) |
| `MaritalStatus` | Single or Partnered |
| `Usage` | Average number of times the treadmill is used per week |
| `Income` | Annual income in USD |
| `Fitness` | Self-rated fitness (1 = Poor to 5 = Excellent) |
| `Miles` | Expected miles to walk/run per week |

### 💰 Product Portfolio
| Product | Description | Price |
|:----------|:-------------|:------|
| **KP281** | Entry-level treadmill | $1,500 |
| **KP481** | Mid-level treadmill | $1,750 |
| **KP781** | Advanced treadmill with premium features | $2,500 |

---

## 🧮 Solution Approach

### 1️⃣ Data Understanding and Cleaning
- Import dataset and check structure (`.info()`, `.shape()`).
- Handle missing values.
- Identify data types of each variable.

### 2️⃣ Outlier Detection
- Use **boxplots** to visualize outliers.
- Clip continuous variables between 5th and 95th percentiles using `np.clip()`.

### 3️⃣ Exploratory Data Analysis (EDA)
- Examine relationships between:
  - **Categorical vs Product** → `countplot()`
  - **Continuous vs Product** → `scatterplot()`
- Example: Relationship between Income, Fitness, and Product.

### 4️⃣ Probability Analysis
- Compute **marginal probabilities** (percentage of customers purchasing each product).
- Build **two-way contingency tables** using `pd.crosstab()`.
- Calculate **conditional probabilities**, e.g.:
  - P(KP481 | Female)
  - P(KP281 | Married)
  - P(KP781 | Fitness Level ≥ 4)

### 5️⃣ Correlation Analysis
- Find correlations among numerical features using `.corr()`.
- Display relationships with a **heatmap** using `seaborn.heatmap()`.

### 6️⃣ Customer Profiling
- Build distinct customer profiles for:
  - KP281
  - KP481
  - KP781
- Segment based on **Age, Income, Fitness, and Usage**.

### 7️⃣ Insights & Recommendations
- Derive actionable recommendations for each product line.

---

## 📊 Key Insights

### 🏃 KP281 – Entry-Level Treadmill
- Purchased by **younger** customers with **lower income**.
- **Fitness Level:** 2–3  
- **Usage:** 2–3 times/week  
- Ideal for **beginners** or **budget-conscious customers**.

### 🧘 KP481 – Mid-Range Treadmill
- Purchased by **middle-income**, often **partnered** customers.
- **Fitness Level:** 3–4  
- **Usage:** 3–4 times/week  
- Suitable for **families** and **regular exercisers**.

### 💪 KP781 – Premium Treadmill
- Preferred by **high-income**, **fitness-focused** individuals.
- **Fitness Level:** 4–5  
- **Usage:** 4–5 times/week  
- Attracts **athletes**, **professionals**, and **premium buyers**.

---

## 💡 Business Recommendations

| Target Segment | Product | Strategy |
|:----------------|:---------|:----------|
| Beginners & young professionals | KP281 | Starter fitness packages, budget offers |
| Families & couples | KP481 | Health subscription bundles, referral offers |
| High-income athletes | KP781 | Personalized services, premium marketing |
| Frequent users | All models | Loyalty rewards & maintenance plans |
| Existing KP281 users | KP481/KP781 | Upgrade offers & membership benefits |

---

## 🧰 Tools & Technologies Used
- **Python Libraries:** pandas, numpy, matplotlib, seaborn  

