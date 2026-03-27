# HR-Analysis-Performance-Compensation-Dashboard
### Project Overview
This project is an end-to-end HR analytics solution built in Power BI, analyzing workforce composition, employee attrition, retention patterns, and compensation performance across an Australian company of 4,200 employees.
The dashboard answers critical HR business questions that help leadership make data-driven decisions around talent retention, salary equity, and workforce planning.
the dataset was presented in an excel format after which i proceeded to load the data into Power Query where i standardized and cleaned the rows and columns, i also assigned them to specific data formats so as to achieve the clear goals of this analysis, also handled some of the null values which were missing and Unprovided with the median, helper column,DataFix and 0 for some specific cases etc.
After cleaning, i went ahead to write multiple Dax measures to answer each of the business Questions presented while bringing clarity to the problems, after that, i went ahead to visualize the findings and trend behaviour overtime which i uncovered while analyzing the data and also the key drivers to these problems.
### Dashboard features 3 interconnected pages | Workforce Overview | Attrition & Retention | Performance and Compensation |

<img width="951" height="532" alt="Screenshot 2026-03-26 164847" src="https://github.com/user-attachments/assets/df703962-058a-49c9-aeae-416de99a74d0" />
<img width="946" height="536" alt="Screenshot 2026-03-26 164932" src="https://github.com/user-attachments/assets/71d9cc25-76b7-4c6c-96bc-3c4bd2215ab3" />
<img width="959" height="540" alt="Screenshot 2026-03-26 165054" src="https://github.com/user-attachments/assets/2fc231b4-a276-4b54-b275-dd469fcce0fa" />

### Dashborad Breakdown
####  Workforce Overview
Provides a high-level snapshot of the entire workforce including headcount, gender distribution, and age demographics.
Key Metrics:

* Total Employees: 4,200
* Male: 2,117 (50.40%) | Female: 2,083 (49.60%)
* Youngest Employee: 20 | Oldest Employee: 60
#### Attrition & Retention
Deep dives into employee turnover, identifying when, where, and why employees are leaving?.

Key Metrics:

* Attrition Rate: 24.64% (1,034 employees)
* Retention Rate: 75.36% (3,166 employees)

Key Insights:

* Perth City leads attrition by city with 199 employees lost
* Attrition peaked at 115 employees in 2015, with a recent surge to 108 in 2024
* Top attrition drivers are evenly distributed: Work-Life Balance, Relocation, Termination, Career Change, and Better Offer, each accounting for 20%

#### Performance & Compensation
Examines the relationship between salary, job role, education level, training hours, and performance ratings.
Key Metrics:

* Total Salary Disbursed: $476M
* Average Salary: $113.43K
* Average Performance Rating: 3.01
* Average Training Hours: 62.08

Key Insights:

* Coordinators earn the highest average salary at $115K, slightly above Managers and Leads
* Bachelors degree holders account for the highest salary pool at $125M
* Salary earnings remain relatively consistent across all performance ratings (1–5), suggesting compensation is not strongly tied to performance scores
* Harry Clark is the top salary earner at $2,525,991 in total disbursed salary

####  Tools & Technologies
|Tool | Usage |
* Power BI Desktop = |Dashboard design| data modeling| DAX measures|
* Power Query = |Data transformation and cleaning|
* DAX = |Custom measures | KPI calculations|
#### Dax Measures Used
(Attrition Rate)
Attrition Rate % = 
DIVIDE(
    COUNTROWS(FILTER(Employees, Employees[AttritionStatus] = "Left")),
    COUNTROWS(Employees)
) * 100

(Retention Rate)
Retention Rate % = 100 - [Attrition Rate %]

(Total Salary Disbursed)
Total Salary Disbursed = SUM(Salary[Salary])

(Average Salary)
Avg Salary = AVERAGE(Salary[Salary]) 
And quite a lot more Dax measures.

#### Business Recommendations
* Investigate 2024 attrition spike, the jump to 108 departures after a low of 81 in 2022 calls for immediate HR attention.
* Review Perth City operations, consistently high attrition across cities suggests a location-specific retention problem.
* Tie compensation to performance, flat salary distribution across performance ratings (1 – 5) may be demotivating high performers.
* Diversify attrition interventions, since all 5 attrition drivers share 20% each, a broad retention strategy is actually needed rather than targeting a single cause.

#### How to Use
* Click this link to download the File for this Analysis (Zipped) [Hr data Analysis Main.zip](https://github.com/user-attachments/files/26296683/Hr.data.Analysis.Main.zip)
 in Power BI Desktop
* Navigate between pages using the sidebar bookmark navigator
* Use slicers and filters to explore specific segments

####  Author
##### Anthony Wayas 
Data Analyst | Power BI | Excel | SQL

This project is part of my data analytics portfolio demonstrating end-to-end BI development skills.
