# 📌 Outliers in Machine Learning

## 1. What are Outliers?
Outliers are **data points that differ significantly** from the majority of the data.  
- They lie far away from the general distribution of the dataset.  
- Outliers can occur due to measurement errors, incorrect data entry, or rare events.  

---

## 2. When are Outliers Dangerous?
- Outliers are dangerous when the model is **sensitive to extreme values**, especially in **linear or weight-based models**.  
  - They can cause **overfitting or underfitting**.  
- However, outliers are **useful in anomaly detection tasks** (e.g., fraud detection, medical diagnosis, fault detection).  

---

## 3. Effect of Outliers on ML Algorithms

### ❌ Negative Impact (Sensitive to Outliers)
- **Linear Regression** → shifts regression line towards outliers  
- **Logistic Regression** → biased coefficients  
- **AdaBoost** → focuses too much on misclassified outliers  
- **Deep Learning Models** → gradient explosion due to large errors  

### ✅ Less or No Effect (Robust to Outliers)
- **Tree-based Models**:  
  - Decision Tree  
  - Random Forest  
  - XGBoost  
  - Gradient Boosted Trees  

---

## 4. How to Treat Outliers?

### 🔹 Common Methods
- **Trimming (Remove Outliers)**  
  - ✅ Good: Simple and effective when few outliers  
  - ❌ Bad: Dangerous when many outliers, can lose valuable information  

- **Capping (Winsorization)**  
  - Replace extreme values with nearest percentile thresholds  

### 🔹 Less Common Methods
- **Treat as Missing Values (NaN)** and impute later  
- **Discretization (Binning)**  

---

## 5. How to Detect Outliers?

1. **Normal Distribution (Gaussian Data):**  
   Outliers lie outside  
   ```math
   \mu \pm 3\sigma
# Outlier Detection & Removal

## 📊 For Skewed Distributions

### Boxplot (IQR Rule)
- Outlier if:
  - **Below:** Q1 − 1.5 × IQR  
  - **Above:** Q3 + 1.5 × IQR  

## 📊 For Other Distributions

### Percentile-based Cutoff
- Outlier if:
  - **Below:** 2.5th percentile  
  - **Above:** 97.5th percentile  

---

## 6. Techniques for Outlier Detection & Removal

### 1. Z-score Method (Standardization)
**Formula:**  
\[
Z = \frac{(x - \mu)}{\sigma}
\]  

**Rule:** If |Z| > 3 → Outlier  

---

### 2. IQR-based Filtering
**Range:**  
\[
[Q1 - 1.5 \times IQR,\; Q3 + 1.5 \times IQR]
\]  

---

### 3. Percentile Method
- Keep only values between **2.5th and 97.5th percentile**

---

### 4. Winsorization (Capping)
- Replace extreme values with cutoff thresholds
