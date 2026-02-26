## 📊 Survey Data Cleaning & Analysis Project
📌 Project Overview

This project involved cleaning, transforming, reshaping, and analyzing a large survey dataset containing 106,304 rows and 293 columns. The objective was to efficiently restructure multi-select survey responses and generate meaningful insights using Excel (Power Query) and Python (Pandas).

---

## 🗂️ Data Preparation (Excel – Power Query)

Downloaded and imported dataset into Excel Power Query

Removed unnecessary top rows

Promoted first row to headers

Renamed columns for clarity

Removed irrelevant columns

Retained:

Demographics

Programming Language (Python – Other languages)

IDE (Jupyter – Other IDEs)

Notebooks (Kaggle – Other Notebooks)

Data Visualization (Matplotlib – Others)

After initial cleaning:

Final shape in Excel: 106,302 rows and 122 columns

⚠️ During the Melt (Unpivot) transformation, performance significantly reduced due to dataset size.

To improve processing efficiency:

Exported dataset

Reshaped and transformed using Python (Pandas)

Reloaded for further analysis

---

## 🐍 Data Cleaning in Python (Pandas)
🔎 Null Value Assessment

Used df.isnull() to check missing values:

Column	Null Count
Age	445
Gender	95
Country	121
Education Level	2,983
Current Role	7,214
Experience Years	13,516
🧹 Cleaning Steps

Converted blank cells to NaN

Removed rows where Age, Gender, Country, Education Level, Current Role, Experience Years, and Data Analytics Tool were all blank

Converted NaN values to "Unknown" where appropriate

---

## 🏢 Column Standardization
1️⃣ Company Size

Fixed inconsistent values

Converted blanks → NaN → "Unknown"

2️⃣ Yearly Compensation

Replaced "I do not wish to disclose" → "Undisclosed"

Added $ sign

Fixed inconsistent numbering using dictionary replacement

Converted NaN → "Unknown"

3️⃣ Data Analytics Tool

Converted empty cells → NaN → "Unknown"

---

## 🔄 Data Reshaping (Melting Process)
🔹 First Melt (Respondent Identification)

Stored identifier columns in id_vars

Stored melt columns in a dictionary

Executed melt operation

Dropped NaN values from value column

Reset index to start from 0

📈 Resulting dataset:
914,884 rows and 14 columns

This transformation normalized multi-select survey responses into an analysis-friendly structure.

👤 Sample Respondent Insight

Respondent 1080
An early-career software engineer based in Nigeria 🇳🇬 with strong expertise in:

Python programming

Data analytics tools

Multiple IDE environments

Notebooks & cloud platforms

BI & public sharing platforms

Shows versatility across development and analytics with strong interest in business intelligence and visualization.

---

🔹 Second Melt (Analysis-Ready Dataset)

Purpose: Analyze 3 key survey questions:

Most Used Programming Language

Most Used Visualization Tool

Most Used BI Tool

Enhancements:

Removed nulls inside loop

Introduced new column "Selected" with binary indicator (1)

Simplified aggregation and counting

Aggregated results exported to Excel for Pivot Table & Pivot Chart analysis.

---

📂 Repository Structure

---

```
Global-Developer-Survey-Data-Engineering-BI-Analysis/
│
├── data/
│   ├── raw_survey_data.csv   
│
├── notebooks/
│   └── survey_cleaning_transformation.ipynb
│
├── outputs/
│   └── survey project.xlsx
│
├── Survey analysis.PNG
├── Summary sheet.PNG
│
└── README.md
```
---

## 📊 Dashboard Preview  

### 1️⃣ Survey Analysis Dashboard  
![Survey Analysis](Survey%20analysis.PNG)

---

### 2️⃣ Summary Sheet  
![Summary Sheet](Summary%20Sheet.PNG)

---

## 📊 Analysis Questions Answered

Survey Question by Total Respondent

Survey Question by Gender

Educational Level by Gender

BI Tool by Education Level

Total Respondent by Educational Level

---

## 📈 Key Insights
💻 1️⃣ Survey Question by Total Respondent

Most Used Programming Language: Python

Most Used BI Tools: Power BI and Tableau

Most Used Visualization Tool: Matplotlib

👨‍💼 2️⃣ Survey Question by Gender

Male respondents dominated across all tool categories

Python and SQL showed strong dominance among male respondents

Overall tool usage was significantly higher among males

🎓 3️⃣ Educational Level by Gender

Female: 16.91%

Male: 83.09%

Male respondents dominated across all education levels

Master's degree holders had the highest participation overall

📊 4️⃣ BI Tools by Education Level

Power BI and Tableau show strongest adoption

Highest usage among Bachelor's and Master's degree holders

Indicates BI tools are widely used among formally educated professionals

🎓 5️⃣ Total Respondents by Education Level

Master's degree holders represent the largest group

Followed by Bachelor's degree holders

Doctorate and Professional degrees contribute moderately

High school respondents are significantly lower

📌 This suggests the survey audience is highly educated.

---

## 🛠️ Tools Used

📊 Excel (Power Query, Pivot Tables, Pivot Charts)

🐍 Python (Pandas)

🧮 Data Reshaping (Melt / Unpivot)

📈 Aggregation & Analysis

---

## 🚀 Project Highlights

✔️ Handled large-scale dataset (100k+ rows)
✔️ Improved performance by switching from Excel to Python
✔️ Standardized inconsistent categorical data
✔️ Transformed multi-select survey data into normalized structure
✔️ Generated demographic and tool-usage insights

---

## 📂 Dataset Information & Access

Due to the large file size of the dataset, it has not been uploaded directly to this repository.  
The dataset is stored in my Google Drive, and the access link will be provided below for easy download.

### 📌 Dataset Source
The dataset was obtained from Kaggle.

🔗 Kaggle Dataset Link: [12.	https://www.kaggle.com/datasets/andradaolteanu/kaggle-data-science-survey-20172021]  
🔗 Google Drive Download Link: [13.	https://docs.google.com/spreadsheets/d/1tz-9MQt7XLfQG6LRcQ6wjYFlZ9N5L0ku/edit?usp=sharing&ouid=117224750797928370837&rtpof=true&sd=true]
