# 📘 Assignment-1  
## Learning Probability Density Function 
---

## 📌 Overview

This project focuses on learning the parameters of a probability density function (PDF) after applying a non-linear transformation to real-world air quality data.

The NO₂ feature from the India Air Quality dataset is transformed using a roll-number-parameterized function and then modeled using a Gaussian-type probability distribution.

---

## 📂 Dataset

- **Dataset Name:** India Air Quality Data  
- **Source:** Kaggle  
- **Feature Used:** NO₂  
- Missing values were removed before further processing.

---

## 🔄 Step 1: Data Transformation

Each NO₂ value \( x \) was transformed into \( z \) using:

\[
z = x + a_r \sin(b_r x)
\]

Where:

\[
a_r = 0.05 \times (r \bmod 7)
\]

\[
b_r = 0.3 \times (r \bmod 5 + 1)
\]

- \( r \) = University Roll Number  
- The sine function is evaluated in radians.

---

## 📊 Step 2: Parameter Estimation

The given probability density function is:

\[
\hat{p}(z) = c \cdot e^{-\lambda (z-\mu)^2}
\]

This follows the form of a Gaussian distribution.

Parameters were estimated using:

- **Mean (μ)** = Average of transformed data (z)
- **Variance (σ²)** = Variance of transformed data (z)

From variance:

\[
\lambda = \frac{1}{2\sigma^2}
\]

\[
c = \frac{1}{\sqrt{2\pi\sigma^2}}
\]

---

## 📈 Visualization

- A histogram of transformed values (z) was plotted.
- The estimated PDF curve was overlaid for comparison.
- The distribution shows slight right skewness due to real-world NO₂ characteristics.

---

## 🛠 Tools Used

- Python
- Pandas
- NumPy
- Matplotlib
- Google Colab

---

## ✅ Output

The following parameters were computed:

- μ (Mean)
- λ (Lambda)
- c (Constant)

These values represent the learned probability density function for the transformed dataset.

---

## 📌 Conclusion

The transformed NO₂ data was successfully modeled using a Gaussian-type probability density function. The parameters were estimated using statistical methods based on the transformed data.
