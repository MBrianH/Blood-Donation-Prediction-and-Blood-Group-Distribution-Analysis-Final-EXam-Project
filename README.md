
# 🩸 Blood Donation Prediction and Blood Group Distribution Analysis

## 👨‍💻 Author
- **Name**: Mutsinzi Brian Heritier  
- **Group**: Group B  
- **Lecturer**: Mr. Maniraguha Eric

---

## 📌 Project Overview
This project provides a comprehensive analysis of blood donation trends across Malaysian states. It combines data cleaning, exploratory analysis, clustering, and dashboard visualization to support better planning and decision-making in blood bank management.

Through Python-based analytics and a Power BI dashboard, the project delivers insights into which states donate the most, how different blood types behave across time, and how regions cluster based on their donation behavior.

---

## 🎯 Objectives
- 🩸 Identify high and low donating states
- 📈 Track donation trends over time by blood type
- 🧠 Cluster states with similar donation behaviors using machine learning
- 📊 Communicate insights through interactive dashboards

---

## 📁 Dataset
### 🔸 [blood_donations_state.csv](https://github.com/user-attachments/files/21571605/blood_donations_state.csv)
| Column Name  | Description                            |
|--------------|----------------------------------------|
| `date`       | Date of the donation                   |
| `state`      | Malaysian state name                   |
| `blood_type` | Blood type (A, B, AB, O, or ALL)       |
| `donations`  | Number of donations recorded           |


## 🧪 Python Analysis Summary

### 1️⃣ Clean the Dataset
- Convert `date` to datetime
- Remove missing/invalid records
- Filter out aggregate blood type entries (`ALL`)
- Pivot dataset to wide format: `blood_a`, `blood_b`, `blood_ab`, `blood_o`
- Detect and flag outliers using a custom IQR method

  <img width="486" height="536" alt="clean dataset Handle missing values, inconsistent formats, and outliers " src="https://github.com/user-attachments/assets/14d02380-c0dd-4682-8c35-8a6255a129cd" />

OUTPUT:
<img width="520" height="136" alt="clean dataset Handle missing values, inconsistent formats, and outliers  output" src="https://github.com/user-attachments/assets/b738795b-1f99-4f12-bd79-6906851c9cf6" />

<img width="864" height="64" alt="export cleaned dataset to csv" src="https://github.com/user-attachments/assets/4162e358-884a-4864-9f11-d7f66dacebde" />


### 2️⃣ Exploratory Data Analysis (EDA)
- Statistical summaries of blood donations by group
- 
  <img width="535" height="522" alt="Conduct Exploratory Data Analysis (EDA)  Generate descriptive statistics  " src="https://github.com/user-attachments/assets/fdaa1cf3-9f05-441f-9685-e9c15a8edf1e" />

  OUTPUT
  <img width="534" height="481" alt="Conduct Exploratory Data Analysis (EDA)  Generate descriptive statistics   output" src="https://github.com/user-attachments/assets/3e507278-e415-4bad-b42b-217adb19e70b" />

- Visualization of distributions (histograms, boxplots)
  histograms Distribution
<img width="735" height="348" alt="Conduct Exploratory Data Analysis (EDA) visualization Histograms (Distribution)" src="https://github.com/user-attachments/assets/931b7366-77ca-4cb1-8db9-1d226f85925f" />

OUTPUT
<img width="830" height="544" alt="Conduct Exploratory Data Analysis (EDA) visualization Histograms (Distribution) output" src="https://github.com/user-attachments/assets/b1a2147f-bf11-468a-85d2-f3f28deb180a" />

 Boxplot
 <img width="584" height="580" alt="Conduct Exploratory Data Analysis (EDA) visualization boxplot" src="https://github.com/user-attachments/assets/32b12966-3096-403b-9dd4-fb08a8cb3851" />

### 3️⃣ K-Means Clustering
- Group by state and average donations by blood type
- Standardize features using `StandardScaler`
- Apply KMeans with `k=3`
- Evaluate using Silhouette Score

Screenshoots

<img width="459" height="615" alt="Clustering Model  Plot elbow curve and output " src="https://github.com/user-attachments/assets/ffde3683-5179-410e-ac2e-70715b8e4c0a" />


<img width="558" height="381" alt="Clustering Model  Apply KMeans with chosen number of clusters AND  output " src="https://github.com/user-attachments/assets/e2cb0ce0-aa69-4f87-8616-f412c750ce39" />

<img width="584" height="588" alt="evaluation metrics   silhouette score" src="https://github.com/user-attachments/assets/67afcd47-f4ad-4b3b-b8d4-d28aee6e0264" />

---

## 📊 Power BI Dashboard

An interactive dashboard visualizing the dataset:
- Filled Map for geographic donation volumes
- Time series by month and year
- Stacked column chart of blood type distribution
- Slicers for filtering by state, year, and blood type
screenshoots:
<img width="864" height="490" alt="dashboard overview" src="https://github.com/user-attachments/assets/d07e7141-99ce-44f4-ab35-1ac125feddaf" />

<img width="897" height="495" alt="dashboard " src="https://github.com/user-attachments/assets/f99571c6-ed8d-42d7-8815-29a2885f43d0" />

POWER BI DOWNLOADABLE FILE:https://tinyurl.com/POWER-BI-FILES
---

## 🎥 PowerPoint Presentation
[Blood_Donation_Capstone_Presentation.pptx](https://github.com/user-attachments/files/21571566/Blood_Donation_Capstone_Presentation.pptx)

- Covers problem, objectives, methodology, analytics, insights, and conclusions

---

## 🌟 Innovation Highlight
This project includes a **custom IQR-based anomaly detection module** to find extreme or unexpected donation patterns. This adds an additional layer of insight into regional behaviors and possible data quality issues.

---

## 🧠 Suggested Improvements
- Integrate time-series forecasting (e.g., ARIMA or Prophet)
- Compare K-Means with hierarchical clustering or DBSCAN
- Use demographic factors if available (age, gender)

---


