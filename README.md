# 🧠 Analysing-Student's-Mental-Health

#### 🛠️ Tool Used: SQL
#### Dataset Source: DataCamp

## ⚽️ Project Goal:
This project explores the mental health challenges faced by international students in Japan, focusing on factors such as social connectedness, acculturative stress, and depression levels. The study aims to validate prior research findings that international students face a higher risk of mental health difficulties and assess whether the length of stay affects mental health outcomes.
## 📂 Dataset Information
- Data collected from international students in Japan (2018).
- Key features:
  - Social Connectedness (SC): Sense of belonging to a group.
  - Acculturative Stress (AS): Stress of adapting to a new culture.
  - Depression Levels (PHQ): Measured using the PHQ-9 depression scale.
  - Length of Stay: Duration of study abroad experience.
## 🛠️ Techniques Used
- SQL Queries for Data Analysis
- Data Aggregation & Filtering
- Exploratory Data Analysis (EDA)

## 🔍 Key Insights Extracted:
- International students showed higher rates of depression than the general population.
- A strong correlation was found between social connectedness and lower depression levels.
- Students with longer stays experienced lower stress levels, suggesting improved adaptation over time.
- Acculturative stress declined as students integrated into their new environment, influencing mental well-being.

## SQL Queries Used:

##### Dataset Preview
**Query:**
````sql
SELECT * 
FROM students;
````
**Result:**
<img width="922" alt="Screenshot 2025-02-20 at 13 53 06" src="https://github.com/user-attachments/assets/16d5a3fb-476f-46d2-ba91-1643313d2c10" />
##### To assess the impact of length of stay on depression and stress.
**Query:**
````sql
SELECT stay, COUNT(*) AS count_int, 
    ROUND(AVG(todep), 2) AS average_phq,
    ROUND(AVG(tosc), 2) AS average_scs, 
    ROUND(AVG(toas), 2) AS average_as
FROM students
WHERE (inter_dom = 'Inter')
GROUP BY stay
ORDER BY stay DESC
LIMIT 9;
````
## 📌 Business/Research Implications & Recommendations
- Universities should provide mental health resources tailored for international students.
- Cultural adaptation programs can reduce acculturative stress.
- Early intervention strategies should be implemented for students at risk.

