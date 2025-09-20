# 🧠 Analysing-Student's-Mental-Health

#### 🛠️ Tool Used: SQL
#### Dataset Source: DataCamp
#### 📂 Dashboard Link: [View Here](https://www.datacamp.com/datalab/w/db1e8505-a537-4799-80f3-873ad8b4a412/edit#3b05e587-87e3-4bec-9511-ddaae6552ac4)
#### Case Study Report: [View Here](https://www.canva.com/design/DAGyOEr_TwE/ONa17X-pm2ZQPvLTk1hBUQ/view?utm_content=DAGyOEr_TwE&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hc0e3474114)

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
<img width="918" alt="Screenshot 2025-02-20 at 14 01 56" src="https://github.com/user-attachments/assets/6526d8ef-30b0-41f6-afe9-648d4ff7285c" />

## 📌 Business/Research Implications & Recommendations
- Universities should provide mental health resources tailored for international students.
- Cultural adaptation programs can reduce acculturative stress.
- Early intervention strategies should be implemented for students at risk.

<img width="918" alt="Screenshot 2025-02-20 at 14 01 56" src="https://github.com/user-attachments/assets/6526d8ef-30b0-41f6-afe9-648d4ff7285c" />
<img width="1920" height="1080" alt="12" src="https://github.com/user-attachments/assets/658f8c9e-eea8-48e1-a1af-70ed48a81ac3" />
<img width="1920" height="1080" alt="11" src="https://github.com/user-attachments/assets/161d22b8-f4d6-4241-84cc-2d890ed76d64" />
<img width="1920" height="1080" alt="10" src="https://github.com/user-attachments/assets/1f847dcd-f24b-44d4-b179-31b1e0ee856c" />
<img width="1920" height="1080" alt="9" src="https://github.com/user-attachments/assets/6e200287-b71e-4725-b6e1-4f21ea4388e3" />
<img width="1920" height="1080" alt="8" src="https://github.com/user-attachments/assets/59d6275c-b419-4f42-aff7-357ec070b1d5" />
<img width="1920" height="1080" alt="7" src="https://github.com/user-attachments/assets/2bd2a71b-e679-4b98-91ff-817cd899314c" />
<img width="1920" height="1080" alt="6" src="https://github.com/user-attachments/assets/dd9f8e2c-ea3d-4c36-b6ea-daf82ffff712" />
<img width="1920" height="1080" alt="5" src="https://github.com/user-attachments/assets/7183cbf4-f8fd-4384-9ba0-0c534e82f9c3" />
<img width="1920" height="1080" alt="4" src="https://github.com/user-attachments/assets/ef4ad852-0eee-4239-9918-c3bbf72b3e82" />
<img width="1920" height="1080" alt="3" src="https://github.com/user-attachments/assets/6ed70aec-cb37-4444-bd19-9915e7626d0e" />
<img width="1920" height="1080" alt="2" src="https://github.com/user-attachments/assets/d4603ecb-909b-4f55-9c0c-2a998fe02011" />
<img width="1920" height="1080" alt="1" src="https://github.com/user-attachments/assets/6dfa44e2-e1a5-471a-921d-5f9425757db6" />



