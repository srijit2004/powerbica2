# Social Media Usage & Digital Wellbeing Dashboard

**Author:** Shruti Somvanshi  
**Registration Number:** 12310394  
**Subject:** INT374 : DATA ANALYTICS WITH POWER BI

---

## Project Overview
This repository contains a Power BI dashboard that analyzes social media usage, behavioral patterns, productivity impact and mental wellbeing. The dashboard transforms raw survey data into visual insights on average daily screen time, platform preferences, stress & sleep relationships, job satisfaction, and digital wellbeing settings.

Key highlights (from the dashboard):
- **Avg Daily Social Media Time:** 3.3 hrs/day  
- **Most Used Platform:** TikTok  
- **Average Breaks During Work:** 1.3 hrs/day  
- **Average Screen Time per Day:** 3.34 hrs  
- **Job Satisfaction Score (avg):** 4.96  
- **Total Male Count:** 8427  
- **Total Female Count:** 8342

---

## Dashboard Pages & Visuals
The Power BI file is split into multiple pages — each designed with a clear narrative and interactive filters.

1. **Main Page / Dashboard Overview**
   - KPI cards for average screen time, most used platform, average breaks and average daily social media time.
   - Age-group and gender breakdowns (bar chart + donut).
   - Filters: Age Group, Gender, Job Type, Platform, Digital Wellbeing Enabled.

2. **Behavioural Patterns / Productivity & Mental Wellbeing**
   - Scatter/line charts showing relationship between screen time before sleep and stress levels.
   - Area/line chart for social media usage vs sleep hours.
   - Visuals showing average burnout and sleep based on coffee intake and productivity by job type.

3. **Summary Page / Basic Statistics**
   - Tabular summaries of platform counts, number of notifications, sleep hours aggregated by job type and gender.
   - Aggregate numeric KPIs for total users, sums and averages to support insights and reporting.
    



## 🖼️ Screenshots

### **Dashboard Overview**
<img src="https://github.com/Shrutiso/social_media_VS_Productivity_dashboard/blob/main/img-1.png?raw=true" width="600">

---

### **Behaviour & Productivity Insights**
<img src="https://github.com/Shrutiso/social_media_VS_Productivity_dashboard/blob/main/img-2.png?raw=true" width="600">

---

### **Summary & Analysis**
<img src="https://github.com/Shrutiso/social_media_VS_Productivity_dashboard/blob/main/img-3.png?raw=true" width="600">




## Data
The dashboard uses a cleaned and preprocessed survey dataset containing (but not limited to) the following fields:
- `age_group`
- `gender`
- `job_type`
- `social_platform_preference`
- `daily_social_media_time`
- `screen_time_before_sleep`
- `sleep_hours`
- `stress_level`
- `coffee_consumption_per_day`
- `has_digital_wellbeing_enabled`
- `number_of_notifications`
- `breaks_during_work`
- `job_satisfaction_score`


## Measures / Example DAX snippets


```DAX
AvgDailySocialMediaTime = AVERAGE('social_media_productivity'[daily_social_media_time])

AvgBreaksDuringWork = AVERAGE('social_media_productivity'[breaks_during_work])

AvgJobSatisfaction = AVERAGE('social_media_productivity'[job_satisfaction_score])

TotalMaleCount = CALCULATE(COUNTROWS('social_media_productivity'), 'social_media_productivity'[gender] = "Male")
TotalFemaleCount = CALCULATE(COUNTROWS('social_media_productivity'), 'social_media_productivity'[gender] = "Female")



