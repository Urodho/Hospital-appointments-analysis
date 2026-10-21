# Hospital Appointment No-Shows Data Analysis

## 1. Project Overview

This project analyzes hospital appointment data to understand why patients miss scheduled medical appointments and identify factors associated with missed appointments.

Missed appointments are a challenge for healthcare facilities because they can waste medical staff time, reduce the use of available appointment slots, and delay patient care. By analyzing appointment records, hospitals can identify patterns in attendance and explore ways to improve their appointment management systems.

As a beginner Data Analyst, I used Python and its data analysis libraries to clean, explore, analyze, and visualize appointment data to generate insights that can support better healthcare planning and decision-making.

## 2. Problem Statement

Hospitals depend on patients attending their scheduled appointments to provide timely and effective healthcare services. However, some patients fail to attend their appointments without cancelling or rescheduling.

When appointments are missed, healthcare facilities may lose valuable time and resources, while other patients may have to wait longer for medical services.

The main problem addressed in this project is:

**What patterns are associated with missed hospital appointments, and what practical actions could healthcare facilities consider to improve patient attendance?**

## 3. Project Objectives

The objectives of this project are to:

- Calculate the overall missed appointment rate.
- Investigate the relationship between waiting time and missed appointments.
- Compare missed appointment rates between patients who received SMS reminders and those who did not.
- Examine appointment attendance patterns across different age groups.
- Compare missed appointment rates across weekdays.
- Investigate differences in attendance across hospital neighbourhoods.
- Compare appointment attendance by gender.
- Explore relationships between selected patient and appointment characteristics.
- Develop practical, data-driven recommendations for improving appointment attendance.

## 4. Dataset

**Dataset:** Medical Appointment No Shows

**Source:** Kaggle

**Dataset link:** https://www.kaggle.com/datasets/joniarroba/noshowappointments

The dataset contains medical appointment records and information about patients, scheduled appointment dates, appointment dates, SMS reminders, and whether patients attended their appointments.

### Important variables

| Variable | Description |
|---|---|
| `patient_id` | Identifies a patient |
| `appointment_id` | Identifies an appointment |
| `gender` | Patient's recorded gender |
| `scheduled_day` | Date the appointment was scheduled |
| `appointment_day` | Date the appointment was due |
| `age` | Patient's age |
| `neighbourhood` | Area associated with the appointment record |
| `scholarship` | Indicates participation in the recorded welfare programme |
| `hypertension` | Indicates recorded hypertension status |
| `diabetes` | Indicates recorded diabetes status |
| `sms_received` | Indicates whether an SMS reminder was recorded |
| `no_show` | Indicates whether the patient attended |

In the original dataset, `No-show = Yes` means the patient missed the appointment, while `No-show = No` means the patient attended.

## 5. Tools and Technologies

The following tools and libraries were used in the project:

- **Python:** Main programming language.
- **Pandas:** Cleaning, transforming, grouping, and analyzing data.
- **Matplotlib:** Creating charts and visualizations.
- **Seaborn:** Producing statistical visualizations, including a correlation heatmap.
- **Jupyter Notebook:** Organizing and documenting the analysis.
- **Git and GitHub:** Tracking changes and sharing the project.

## 6. Project Workflow

The project follows a structured data analysis process.

### Step 1: Data collection
Obtained the medical appointment dataset from Kaggle.

### Step 2: Data cleaning
- Standardized column names.
- Converted date columns into appropriate date formats.
- Checked for duplicate records.
- Removed invalid age values and records with invalid appointment outcomes.
- Checked appointment dates and removed records with negative waiting periods.

### Step 3: Feature engineering
Created additional variables to support the analysis, including:

- `waiting_days`: Number of days between scheduling and the appointment date.
- `missed`: A binary indicator showing whether an appointment was missed.
- `weekday`: Day of the week of the appointment.
- `age_group`: A category representing the patient's age range.
- `waiting_group`: A category representing the waiting period.

### Step 4: Exploratory data analysis
Used summary statistics and grouped calculations to investigate appointment attendance patterns.

### Step 5: Data visualization
Created charts to communicate the findings clearly and compare missed appointment rates across different categories.

### Step 6: Recommendations
Used the findings to identify possible improvements in appointment reminders, scheduling, and patient communication.

## 7. Key Findings

The following findings are based on the results obtained during the analysis.

### Finding 1: Overall missed appointment rate

The overall missed appointment rate was **20.19%**.

This means approximately one in five recorded appointments was missed.

**Why it matters:** Missed appointments can affect the use of healthcare resources and the availability of appointment slots for other patients.

**Possible action:** Investigate common reasons for missed appointments and consider improving reminder and rescheduling systems.

### Finding 2: Waiting time and missed appointments

The analysis produced the following results:

| Waiting period | Appointments | Missed rate |
|---|---:|---:|
| Same day | 38,562 | 4.65% |
| 1–7 days | 32,185 | 24.15% |
| 8–30 days | 29,396 | 31.72% |
| 31–60 days | 8,283 | 34.15% |
| Over 60 days | 2,095 | 28.45% |

Same-day appointments had the lowest missed rate at 4.65%, while appointments scheduled 31–60 days in advance had the highest rate at 34.15%.

**Why it matters:** The results suggest that longer waiting periods are associated with higher missed appointment rates in several waiting-time categories.

**Possible action:** Consider sending reminders closer to appointment dates, making rescheduling easier, and investigating barriers faced by patients who wait several weeks.

### Finding 3: SMS reminders and missed appointments

| Reminder status | Appointments | Missed rate |
|---|---:|---:|
| No SMS | 75,039 | 16.70% |
| SMS received | 35,482 | 27.57% |

The missed appointment rate was higher among patients recorded as having received an SMS reminder.

**Why it matters:** This unexpected result shows that the presence of a recorded SMS reminder alone does not guarantee attendance.

**Possible action:** Investigate reminder delivery, timing, and patient circumstances. Compare similar patient groups before drawing conclusions about reminder effectiveness.

**Important limitation:** These results show an association, not proof that SMS reminders cause missed appointments.

## 8. Visualizations

The project uses eight visualizations to investigate different aspects of appointment attendance.

1. **Overall Appointment Outcomes — Bar Chart:** Compares attended and missed appointments to show the overall attendance pattern.
2. **Waiting Time vs. Missed Rate — Bar Chart:** Compares missed appointment rates across waiting-time categories.
3. **SMS Reminders vs. Missed Rate — Bar Chart:** Examines differences in missed rates between reminder groups.
4. **Age Groups vs. Missed Rate — Bar Chart:** Compares attendance patterns across age categories.
5. **Weekday vs. Missed Rate — Bar Chart:** Identifies days with relatively higher or lower missed appointment rates.
6. **Neighbourhood vs. Missed Rate — Horizontal Bar Chart:** Highlights the ten neighbourhoods with the largest appointment counts and compares their missed rates.
7. **Gender vs. Missed Rate — Bar Chart:** Compares recorded missed appointment rates by gender.
8. **Correlation Heatmap — Heatmap:** Explores correlations between selected numerical variables and the missed appointment indicator.

Each chart is intended to answer a specific analytical question and communicate a finding that can inform further investigation.

## 9. Recommendations

Based on the findings available so far, the following actions could be considered by healthcare facilities:

- **Improve patient reminders:** Evaluate reminder timing, delivery, and clarity.
- **Make rescheduling easier:** Provide patients with simple ways to change appointment dates.
- **Investigate long waiting periods:** Examine whether scheduling delays, patient circumstances, or other factors are associated with missed appointments.
- **Study the SMS result further:** Compare patients with similar waiting periods and other characteristics before evaluating reminder effectiveness.
- **Monitor attendance patterns:** Regularly review missed appointment rates by waiting period, weekday, age group, and neighbourhood.
- **Collect feedback:** Ask patients about barriers that prevent them from attending appointments.

These recommendations should be evaluated using further analysis and, where possible, follow-up studies before implementation.

## 10. Limitations of the Analysis

This project has several limitations:

- The dataset does not directly explain why each patient missed an appointment.
- Observed relationships do not establish cause and effect.
- The higher missed rate among SMS recipients may be influenced by differences between patient groups.
- Some relevant factors, such as transport difficulties, work schedules, and personal circumstances, may not be recorded.
- Results from this dataset may not represent every hospital or healthcare system.
- Data cleaning decisions may affect the final results.

These limitations are important when interpreting the findings and making recommendations.

## 11. Conclusion

This project demonstrates how data analytics can help healthcare facilities understand appointment attendance patterns.

The analysis found an overall missed appointment rate of 20.19%. Missed rates differed substantially by waiting period, ranging from 4.65% for same-day appointments to 34.15% for appointments scheduled 31–60 days in advance. The analysis also found a higher missed rate among patients recorded as receiving SMS reminders, highlighting the need for further investigation rather than assuming that reminders are ineffective.

The main lesson is that data can reveal patterns that may not be immediately obvious. However, good data analysis requires more than creating charts: analysts must interpret the findings carefully, acknowledge limitations, and recommend practical actions supported by evidence.

The project strengthened my understanding of data cleaning, feature engineering, exploratory data analysis, visualization, and communicating findings in simple language.

## 12. How to Run the Project

1. Clone or download this repository.
2. Install Python if it is not already installed.
3. Install the required libraries:

   ```bash
   pip install pandas matplotlib seaborn jupyter
   ```

4. Download the dataset from Kaggle and place the CSV file in the location expected by the notebook.
5. Open the project notebook in Jupyter Notebook or VS Code.
6. Run the notebook cells in order, from data loading and cleaning through analysis and visualization.

**Note:** The notebook's dataset file path must match the location where the CSV is saved.

## 13. Project Structure

A suggested repository structure is:

```text
hospital-appointment-analysis/
│
├── appointment_analysis.ipynb
├── README.md
├── graphs/
│   ├── graph1_appointment_outcomes.png
│   ├── graph2_waiting_time.png
│   ├── graph3_sms_reminders.png
│   ├── graph4_age_groups.png
│   ├── graph5_weekdays.png
│   ├── graph6_neighbourhoods.png
│   ├── graph7_gender.png
│   └── graph8_correlation_heatmap.png
│
└── .gitignore
```

The filenames above are examples. Update them to match the actual files in your repository.

## 14. Skills Demonstrated

Through this project, I practiced:

- Data cleaning and preprocessing
- Working with dates and time intervals
- Creating calculated columns
- Grouping and aggregating data with Pandas
- Calculating rates and percentages
- Exploratory data analysis
- Data visualization and chart interpretation
- Identifying patterns and communicating insights
- Translating analytical findings into practical recommendations
- Version control and project documentation using Git and GitHub

## 15. Author

**Data Analytics Student**

This project was completed as part of my data analytics learning journey to develop practical skills in Python, data analysis, visualization, and evidence-based decision-making.
