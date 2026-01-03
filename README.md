# Heart Disease Analysis 
## Codecademy Bootcamp - Applied Data Science with Python

![alt text](images/title.png)



## Project Overview
This project investigates patient data from the Cleveland Clinic Foundation to identify factors associated with heart disease. Using statistical analysis and data visualization, we explored how clinical, metabolic, and exercise-related variables relate to heart disease outcomes.

---

## Dataset
The dataset contains information on 303 patients, including the following variables:

- `age`: Age of the patient in years  
- `sex`: Sex assigned at birth ('male' or 'female')  
- `trestbps`: Resting blood pressure (mm Hg)  
- `chol`: Serum cholesterol (mg/dl)  
- `fbs`: Fasting blood sugar > 120 mg/dl (1 = yes, 0 = no)  
- `cp`: Chest pain type ('typical angina', 'atypical angina', 'non-anginal pain', 'asymptomatic')  
- `exang`: Exercise-induced angina (1 = yes, 0 = no)  
- `thalach`: Maximum heart rate achieved during exercise  
- `heart_disease`: Heart disease diagnosis ('presence' = yes, 'absence' = no)  

---

## Analysis Overview

### Part I – Quantitative Variables
- **Cholesterol (chol)**: Patients with heart disease have significantly higher cholesterol levels than patients without heart disease.  
- **Fasting Blood Sugar (fbs)**: 45 out of 303 patients had FBS > 120 mg/dl. Binomial test against population prevalence (8%) gave a p-value of 4.69e-05, indicating a significant difference.  
- **Maximum Heart Rate (thalach)**: Patients with heart disease achieved lower maximum heart rates during exercise, suggesting reduced cardiovascular performance.  
- **Age**: Older patients were significantly more likely to have heart disease.  
- **Resting Blood Pressure (trestbps)**: Also significantly associated with heart disease.  
- **Cholesterol (chol)**: Not significantly associated in some comparisons.  

**Visualizations**: Boxplots for `thalach`, `age`, `trestbps`, and `chol` by heart disease status.

---

### Part II – Categorical Variables
- **Chest Pain Type (cp)**: Strongly associated with heart disease. Asymptomatic patients showed the highest prevalence.  
  - Chi-square test p-value = 2.82e-18 → reject null hypothesis.  
  - Stacked bar plots illustrate prevalence across chest pain types.  
- **Exercise-Induced Angina (exang)**: Patients with exang = 1 had much higher heart disease prevalence.  
  - Stacked bar plots highlight the differences.

**Other Findings**:  
- Combination of clinical symptoms (cp, exang), exercise results (thalach), and metabolic indicators (chol, fbs) provide the clearest assessment of heart disease risk.

---

## Methods
- **Hypothesis Tests**:  
  - Two-sample t-tests for comparing quantitative variables (thalach, age, trestbps, chol)  
  - One-sample binomial test for fasting blood sugar prevalence  
  - Chi-square test for categorical variables (cp, exang)  
  - ANOVA and Tukey HSD for comparisons across multiple groups  
- **Visualization Tools**: `matplotlib`, `seaborn`  
  - Boxplots, stripplots, and stacked bar charts for clear data presentation  

---

## Conclusions
1. Heart disease patients have **lower maximum heart rates**, **higher cholesterol**, **higher fasting blood sugar**, and are generally **older**.  
2. **Chest pain type** and **exercise-induced angina** are strong clinical indicators of heart disease.  
3. Effective heart disease assessment requires **integration of metabolic, clinical, and exercise-related variables**.  

---

## Technologies Used
- Python 3  
- pandas, numpy, scipy.stats  
- matplotlib, seaborn  
- Jupyter Notebook  

---

## Author
**Nataliya Kuznetsov** 

