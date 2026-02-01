# Heart Disease Analytics: End-to-End Analysis & Prediction 

##  Project Overview
Heart disease is still a major killer worldwide. This project connects raw medical data to actual useful insights. 

I used **Python** to do the heavy lifting—cleaning the data and finding patterns—and **Power BI** to visualize the story. The goal wasn't just to guess who is sick, but to give doctors clear signs (like Chest Pain type or Heart Rate) to look for during a diagnosis.

##  Tech Stack
![Python](https://img.shields.io/badge/Python-3.9+-blue?style=for-the-badge&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-150458?style=for-the-badge&logo=pandas)
![Power BI](https://img.shields.io/badge/Power%20BI-Visualization-F2C811?style=for-the-badge&logo=powerbi)

* **Analysis:** Python (Pandas, NumPy)
* **Charts:** Matplotlib, Seaborn
* **Reporting:** Power BI
* **Code Editor:** Jupyter Notebook

---

##  Dashboard Preview
*Here is what the final interactive report looks like.*

![Dashboard Main View](https://github.com/roegzychux/Heart-disease-analytics/blob/5456cd8ad061f30a967a6431e11b2d2cbeb0c5d8/images/Dashboard%201.png)
*(Screenshot: Main Dashboard View)*

![Dashboard Deep Dive](https://github.com/roegzychux/Heart-disease-analytics/blob/5456cd8ad061f30a967a6431e11b2d2cbeb0c5d8/images/Dashboard%202.png)
*(Screenshot: Detailed Clinical Analysis View)*

---

##  Findings: What the Data Actually Says
*I found these patterns while digging through the data in `EDA on Health Disease.ipynb`.*

### 1. The Age "Dip" (Survivorship Bias)
It's obvious that getting older increases the risk. But looking at the data, the number of sick people peaks in the **50-60 and 60-70 age groups** and then drops off for the oldest group.
* **Why?** It's not that people get healthier at 80. It's likely that people with severe heart conditions sadly don't live long enough to be in that oldest bracket. So, the dataset shows fewer of them.

### 2. The Gender Gap
Men are way more likely to be diagnosed with heart disease in this dataset than women. Being male is a massive risk factor on its own here.

### 3. The "Silent" Chest Pain
This was the most important find. You would expect severe chest pain ("Typical Angina") to be the biggest red flag. But actually, patients with **"Asymptomatic"** chest pain (no pain at all) often had heart disease. This is dangerous because they don't feel sick, so they might not get tested.

---

##  4 Key Insights & Recommendations for Doctors
*Here is how a medical team can actually use these numbers.*

1.  **Max Heart Rate is a Huge Clue**
    * **The Data:** Sick patients consistently failed to reach a high heart rate during stress tests.
    * ** Recommendation:** If a patient can't get their heart rate up during a test, treat it as a major warning sign. Even if they say they feel fine, investigate it.

2.  **Pain During Exercise = Danger**
    * **The Data:** If chest pain starts specifically *during* a workout, it's highly linked to heart disease.
    * ** Recommendation:** Prioritize patients who feel pain when moving or exercising. This is a much stronger indicator than random pain while sitting down.

3.  **Blood Pressure Alone Doesn't Tell You Much**
    * **The Data:** High Resting Blood Pressure (BP) didn't really separate the sick people from the healthy ones. Both groups had similar averages.
    * ** Recommendation:** Don't rely on BP alone. A patient with "normal" blood pressure can still be very sick. You have to look at it alongside Age and Cholesterol.

4.  **The Cholesterol Trap**
    * **The Data:** Moderate cholesterol levels were common in both healthy and sick people. But *very* high cholesterol was almost always bad news.
    * ** Recommendation:** Use cholesterol as a secondary check. Don't panic over moderately high levels unless other signs (like age or exercise pain) are present.

---

##  Dashboard Metrics
*The main numbers I track on the Power BI report:*

* **Total Patients:** How many people were in the study.
* **Average Patient Age:** To see if the group leans old or young.
* **Disease Prevalence Rate:** What percentage of people actually had the disease.
* **Average Resting BP:** Tracked across different groups.

---


##  How to Run This Project

### What You Need
* Python 3 installed
* Power BI Desktop (to open the dashboard file)

### Step-by-Step guide
1.  **Get the Code**
    Clone this repo to your computer:
    ```bash
    git clone [https://github.com/yourusername/heart-disease-analytics.git](https://github.com/yourusername/heart-disease-analytics.git)
    ```

2.  **Install the Libraries**
    You need these python tools to run the notebook:
    ```bash
    pip install pandas matplotlib seaborn jupyter
    ```

3.  **Check the Analysis**
    Open the notebook to see how I broke down the numbers:
    ```bash
    jupyter notebook "Notebooks/EDA on Health Disease.ipynb"
    ```

4.  **Open the Dashboard**
    * Go to the `Dashboards` folder.
    * Double-click `HeartDisease.pbix`.
    * It will open in Power BI. You can click the buttons (Slicers) to filter patients by Age, Gender, or Blood Sugar.

