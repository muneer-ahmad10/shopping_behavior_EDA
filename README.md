# shopping_behavior_EDA
The objective of this Exploratory Data Analysis (EDA) is to understand the structure, quality, and patterns within the customer purchase dataset before proceeding to any machine learning modeling. The analysis focuses on numerical distributions, categorical feature balance, relationships between variables, and potential biases in the dataset.


# 📊 Customer Purchase Behavior – Exploratory Data Analysis (EDA)

## 📌 Project Overview

This project performs an in-depth **Exploratory Data Analysis (EDA)** on a customer purchase behavior dataset. The primary goal is to understand the dataset structure, identify patterns, check data quality, and uncover insights that will guide meaningful machine learning modeling.

The analysis focuses on:

* Distribution of numerical features
* Balance and imbalance in categorical features
* Relationships between variables
* Potential biases and modeling implications

---

## 📂 Dataset Description

The dataset contains customer demographic details, purchase behavior, and transaction-related attributes.

### 🔢 Numerical Features

* Age
* Purchase Amount (USD)
* Review Rating
* Previous Purchases

### 🏷️ Categorical Features

* Gender
* Items Purchased
* Size
* Color
* Season
* Subscription Status
* Shipping Type
* Discount Applied
* Promo Code
* Payment Method
* Frequency of Purchases

---

## 🔍 Exploratory Data Analysis

### 1️⃣ Numerical Feature Analysis

#### 📦 Distribution & Outliers

* Boxplot analysis revealed **no significant outliers** across all numerical features.
* All numeric variables are **well-distributed and stable**.

#### 📐 Skewness Analysis

* Skewness values for all numerical features are **very close to zero**.
* Indicates **highly symmetric distributions**.
* No transformation (log, Box-Cox, power transform) is required.

#### 🔗 Correlation Analysis

* Correlation coefficients between numerical features are **near zero**.
* Indicates **no strong linear relationships** among variables.

#### 🔍 Pairplot Analysis

* Pairplots show **random dispersion** with no visible trends or clusters.
* Confirms that numerical features are largely **independent**.
* `Customer ID` was identified as a non-informative feature and excluded from analytical interpretation.

---

### 2️⃣ Categorical Feature Analysis

#### ✅ Balanced Categorical Features

The following features show **uniform category distribution**, indicating no sampling bias:

* Items Purchased
* Color
* Season
* Shipping Type
* Payment Method
* Frequency of Purchases

#### ⚠️ Imbalanced Categorical Features

The following features exhibit **clear imbalance**:

* Gender (Male > Female)
* Size (Medium dominates; XL least frequent)
* Subscription Status (Non-subscribers dominate)
* Discount Applied (Mostly No)
* Promo Code (Mostly Not Used)

These imbalances should be considered during modeling and evaluation.

---

### 3️⃣ Gender-wise Purchase Analysis

#### 🔢 Total Purchase Amount

* Male customers contribute a higher **total purchase amount**, primarily due to higher representation in the dataset.

#### 📊 Average Purchase Amount

| Gender | Average Purchase Amount (USD) |
| ------ | ----------------------------- |
| Female | 60.25                         |
| Male   | 59.54                         |

* Female customers spend **slightly more per purchase on average**.
* The difference is minimal, indicating **similar spending behavior across genders**.

---

## 🧠 Key Insights

* The dataset is **clean, stable, and well-structured**.
* Numerical features show:

  * No outliers
  * Near-zero skewness
  * No strong correlations
* Several categorical features are balanced, while others show clear imbalance.
* Higher total spending by males is driven by **count dominance**, not higher individual spending.
* Overall customer behavior appears **consistent across demographic groups**.

---

## 🤖 Implications for Machine Learning

* Minimal preprocessing is required for numerical features.
* Feature scaling can be applied directly.
* Categorical imbalance should be considered when:

  * Selecting evaluation metrics
  * Interpreting model performance
* Dataset is suitable for:

  * Regression models
  * Classification models
  * Clustering and segmentation tasks

---

## ✅ Conclusion

This exploratory data analysis successfully uncovered the key characteristics of the dataset, verified data quality, identified imbalances, and validated the independence of numerical variables. The dataset is well-prepared for further feature engineering and machine learning modeling.


