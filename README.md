# Overview

This project presents an interactive HR Performance Dashboard developed in Tableau to help HR teams monitor employee attrition and performance metrics across the organization. The dashboard visualizes attrition by department, job role, and age group, alongside employee job satisfaction and work-life balance scores. It incorporates key Tableau features such as dual-axis charts, hierarchies, calculated fields, and dashboard-wide filters. This repository includes the Tableau workbook (.twbx) file containing all interactive visualizations used for monitoring and analysis.

# Tools Used

- **Tableau Desktop**
- **Tableau Public**
- **Microsoft Excel**

# Dashboard Visuals & Business Insights

1. **Attrition Rate by Department & Job Role (Bar Chart)**

![image](https://github.com/user-attachments/assets/dcab4046-20d6-4d19-ab49-7b66169c7477)

This chart displays attrition rates across departments and job roles. The "Department" and "Job Role" fields are used as a hierarchy on the X-axis. Employee count is plotted using COUNT(EmployeeNumber) and color-coded by attrition status. A calculated field for attrition rate is added as a second axis using a dual-axis chart setup. The axes are synchronized and formatted for readability.

2. **Attrition Rate by Age Group (Line Chart)**

![image](https://github.com/user-attachments/assets/6970d7df-2f49-45d0-913f-82d4b7364a72)

This chart visualizes attrition patterns by age brackets. "Age" is grouped into 5-year intervals, and COUNT(EmployeeNumber) is used to show total employees per group. Attrition is color-coded (Yes/No), and a second calculated axis plots the attrition rate using a dual-line chart. The lines are formatted with labels for clarity.

3. **Job Satisfaction & Attrition (Stacked Bar Chart)**

![image](https://github.com/user-attachments/assets/0ccc923b-85ba-45c6-9892-98b8b47319fb)

Job satisfaction scores (1–4) are displayed on the X-axis, with stacked bars representing the percentage of employees who stayed vs. left. The "Attrition" field is used to split the bars by color (red = left, green = stayed). A quick table calculation is applied to show values as percentages.

4. **Work-Life Balance by Department (Tree Map)**

![image](https://github.com/user-attachments/assets/ed95007a-3322-4994-8460-30d82978c575)

Each department is represented as a block, sized by the number of employees and colored based on the average Work-Life Balance score. A gradient color scale (red to green) is used to reflect poor to excellent balance. Labels include department names and scores, and font sizes are adjusted for visibility in smaller blocks.

# Summary KPIs

At the top of the dashboard, three summary tiles highlight key metrics:

- **Attrition Rate (%)**
COUNT(IF [Attrition] = "Yes" THEN [EmployeeNumber] END) / COUNT([EmployeeNumber])
  
- **Average Work-Life Balance**
AVG(WorkLifeBalance)
  
- **Average Job Satisfaction**
AVG(JobSatisfaction)

These KPIs offer quick insight into organizational health and help HR teams act on areas needing attention.

# Final Dashboard

![image](https://github.com/user-attachments/assets/ad50d822-153b-4226-b6e6-0d2c5e3d18c9)

*View the Interactive Dashboard on Tableau Public:* https://public.tableau.com/app/profile/mandar.nadkarni/viz/HRDashboardforPerformanceandAttritionMonitoring/HRPerformanceDashboard

# Interactive Filters

The dashboard includes two filters:

- Department – Allows analysis of specific departments.
- Attrition – Toggle to view only employees who stayed or left.

Filters are applied across all charts to maintain consistency and support dynamic exploration.

# Why These KPIs Matter

These KPIs offer at-a-glance insights into the organization’s HR health:

- Attrition Rate (%) enables HR to monitor employee turnover trends and detect early signs of workforce disengagement.
- Average Work-Life Balance helps uncover stress zones within the organization where employees may be overburdened.
- Average Job Satisfaction reflects how employees perceive their roles, management, and growth opportunities.

Together, these KPIs guide data-driven decisions to improve retention and workplace satisfaction

# Business Questions Answered

This dashboard helps HR managers answer critical business questions. Each is linked to a specific chart for visual insight:

Which department has the highest employee attrition rate?

🔗 Chart: Attrition Rate by Department & Job Role (Bar Chart)

➤ Helps HR target retention strategies effectively by identifying at-risk departments.



Are younger employees more likely to leave the company?

🔗 Chart: Attrition Rate by Age Group (Line Chart)

➤ Allows HR to develop retention programs tailored for younger age brackets.



How does work-life balance impact employee retention?

🔗 Chart: Work-Life Balance by Department (Tree Map)

➤ Identifies departments with poor balance, where policy changes could improve retention.



Does job satisfaction affect attrition?

🔗 Chart: Job Satisfaction & Attrition (Stacked Bar Chart)

➤ Highlights correlation between low satisfaction and high attrition rates.

# Additional Features

- Custom calculated field for Attrition Rate.
- Dual-axis charts to compare employee count and attrition percentage.
- Hierarchical fields to drill down from Department to Job Role.
- Dynamic summary tiles for key HR metrics.
- Tree Map layout to convey work-life balance variations visually

# Conclusions

This Tableau dashboard empowers HR leaders with visual, interactive insights into the state of their workforce. By highlighting attrition patterns, job satisfaction levels, and work-life balance concerns, the dashboard becomes a decision-support tool for retaining top talent and improving employee experience. With built-in filters and KPIs, it ensures actionable, department-specific insights for data-driven HR strategies.
