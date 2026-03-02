# 📊 Derivable Judgement  
## A Complete Statistical Decision-Making Model

---

## 📌 Project Overview

This project demonstrates how inferential statistics is used to derive meaningful judgments from sample data.

A synthetic healthcare dataset was generated and analyzed using multiple statistical techniques including confidence intervals, hypothesis testing, Chi-square test, ANOVA, covariance, and correlation.

The goal of this project is to bridge theoretical statistical concepts with practical implementation in Python.

---

# 🎯 Objective

- Apply inferential statistical methods
- Perform hypothesis testing correctly
- Compute and interpret confidence intervals
- Understand statistical decision rules
- Analyze relationships between variables
- Make data-driven conclusions

---

# 📚 Part A – Theoretical Foundation

## 1️⃣ Inferential Statistics

Inferential statistics allows us to make conclusions about a population using sample data.

Instead of studying the entire population, we:
- Collect a sample
- Analyze it
- Make generalizations

---

## 2️⃣ Hypothesis Testing

Hypothesis testing is a statistical method used to decide whether there is enough evidence to reject a claim about a population.

### Steps:
1. State hypotheses
2. Choose significance level (α)
3. Calculate test statistic
4. Find p-value
5. Make decision

---

## 3️⃣ Null and Alternative Hypothesis

- **Null Hypothesis (H₀):** No effect / No difference / No association
- **Alternative Hypothesis (H₁):** Effect / Difference / Association exists

Example:
H₀: Mean BMI of males = Mean BMI of females  
H₁: Mean BMI of males ≠ Mean BMI of females  

---

## 4️⃣ Type I and Type II Errors

- **Type I Error:** Rejecting a true H₀ (False positive)  
- **Type II Error:** Failing to reject a false H₀ (False negative)

Significance level (α) controls Type I error.

---

## 5️⃣ p-value

p-value is the probability of observing the result assuming H₀ is true.

Decision rule:
- If p-value < α → Reject H₀
- If p-value ≥ α → Fail to Reject H₀

In this project, α = 0.05

---

## 6️⃣ Z-test vs T-test

- **Z-test:** Used when population standard deviation is known.
- **T-test:** Used when population standard deviation is unknown (most real cases).

---

## 7️⃣ Chi-Square Test

Used to test association between categorical variables.

Compares:
Observed frequencies vs Expected frequencies

H₀: Variables are independent  
H₁: Variables are associated  

---

## 8️⃣ ANOVA (Analysis of Variance)

Used to compare means of 3 or more groups.

H₀: All group means are equal  
H₁: At least one group mean differs  

---

## 9️⃣ Covariance and Correlation

- **Covariance:** Shows direction of relationship.
- **Correlation:** Shows strength and direction (-1 to +1).

---

# 📊 Dataset Description

A synthetic healthcare dataset of 120 records was generated.

### Variables:

- `record_id`
- `age`
- `weight`
- `height`
- `bmi`
- `gender`
- `exercise_frequency`
- `hypertension`
- `diabetes`

The dataset simulates real-world health indicators.

---

# 🧪 Statistical Analysis Performed

## 1️⃣ Confidence Interval (Age)

- 95% confidence interval
- Used t-distribution
- Standard error calculated using `stats.sem()`

Interpretation:
We are 95% confident that the true population mean age lies within the calculated interval.

---

## 2️⃣ Critical Value (Two-Tailed Test)

Used:
`stats.t.ppf(1 - 0.05/2, df)`

Purpose:
To determine rejection region for hypothesis testing.

---

## 3️⃣ Independent T-Test (BMI vs Gender)

Tested whether mean BMI differs between males and females.

Method:
`stats.ttest_ind(equal_var=False)`

Decision based on p-value.

---

## 4️⃣ Chi-Square Test (Exercise vs Hypertension)

Tested association between:
- Exercise frequency
- Hypertension status

Method:
`stats.chi2_contingency()`

---

## 5️⃣ One-Way ANOVA (BMI vs Exercise Frequency)

Tested whether BMI differs across:
- Low exercise
- Medium exercise
- High exercise

Method:
`stats.f_oneway()`

---

## 6️⃣ Covariance & Correlation (Age vs BMI)

Analyzed relationship between:
- Age
- BMI

Methods:
- `np.cov()`
- `np.corrcoef()`

---

# 🧠 Decision Rule Used

For all hypothesis tests:

If p-value < 0.05 → Reject H₀  
If p-value ≥ 0.05 → Fail to Reject H₀  

---

# 🛠 Technologies Used

- Python
- NumPy
- Pandas
- SciPy

---

# 📈 Key Learning Outcomes

- Strong understanding of inferential statistics
- Correct application of hypothesis testing
- Ability to interpret statistical outputs
- Practical implementation of statistical theory
- Data-driven decision-making skills

---
