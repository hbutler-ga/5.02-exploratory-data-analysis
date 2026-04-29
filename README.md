# Module 10 — Exploratory Data Analysis (EDA): Understanding Your Data

**Session Time:** 120 minutes

---

## 🎯 Learning Objectives

By the end of this module, you will be able to:

- Understand that **EDA is a process of discovery**, not a fixed sequence of steps  
- Calculate and interpret **measures of central tendency** (mean, median)  
- Evaluate **spread and variability** using standard deviation  
- Explore **categorical variables** using counts and proportions  
- Investigate relationships between variables using **covariance and correlation**  
- Use **Pandas tools** to scale and support your analysis  
- Communicate insights clearly using **code, plots, and written interpretation**

---

## ❓ Guiding Question

> **What factors influence the price of a diamond?**

Throughout this module, we will explore the dataset to answer this question.

---

## 🔍 What is EDA?

Exploratory Data Analysis (EDA) is not a checklist.

It’s not:
- Run `.describe()`
- Make a few plots
- Move on

Instead, EDA is the process of:

> **Asking questions, investigating patterns, and uncovering what your data is actually telling you.**

---

## 🔁 Analytical Mindset

EDA is **iterative**:

1. Ask a question  
2. Explore the data  
3. Discover something new  
4. Refine your question  

This cycle continues until you can confidently explain what’s happening in your dataset.

---

## 📊 Understanding Individual Variables

### Measures of Central Tendency

To understand what is *typical* in your data:

- **Mean** (average):

$$
\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i
$$

- **Median** (middle value in sorted data)

> Mean tells you what’s typical. Median helps when data is skewed.

---

### Spread and Variability

Two datasets can have the same mean but behave very differently.

**Variance** measures how spread out values are:

$$
\text{Var}(X) = \frac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

**Standard deviation** is the square root of variance:

$$
\sigma = \sqrt{\text{Var}(X)}
$$

> Standard deviation tells you how far values typically are from the average.

- Low standard deviation → consistent data  
- High standard deviation → more variability  

---

## 🧩 Exploring Categorical Variables

Not all variables are numeric.

For categorical variables like `cut`, we focus on **distribution**, not averages.

### Frequency

```python
df['cut'].value_counts()