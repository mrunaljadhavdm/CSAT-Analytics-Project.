Customer Satisfaction Analysis Dashboard
CSAT Analytics | DataMites Capstone 1 -- PRDA-02 | Power BI
Project Overview
This project looks at customer support activity and customer
satisfaction using call records from the CSAT dataset. The aim is to
understand when customers contact support, which channels they use, why
they call, how calls are distributed across states, and how
response-time categories are recorded.

The work starts with data connection and preparation, then moves to
Power BI dashboard creation and review of the results. The dashboard
brings the main measures and call patterns together in one place.
Dashboard Preview

Dashboard screenshot:
Screenshots/Customer Satisfaction Dashboard.png
Project Details
  Item             Details
  Project          Capstone 1: PRDA-02 -- CSAT Analytics
Dataset table    project_csat_analytics CSAT
Database         MySQL
Reporting tool   Microsoft Power BI
Records loaded   32,941
Columns loaded   13
Date period      October 2020

Dataset note: The assignment description referred to 32,942 rows and
12 columns. The connected table in Power BI contained 32,941 rows and 13
columns. The figures in this project are based on the data actually
loaded.
Project Objectives
- Review overall customer support call volume.
- Understand the distribution of calls across contact channels.
- Compare call volume by state and reason.
- Review the response-time categories in the dataset.
- Present key measures and patterns in an interactive Power BI
  dashboard.
- Identify practical areas where customer support may be improved.
Tools Used
  Tool                                Purpose
  MySQL                               Source database for the CSAT
records

  Power BI Desktop                    Data preparation, visuals, slicers,
and dashboard
Power Query                         Data type checks, date correction,
and data quality review
Data Preparation
The CSAT table was connected from MySQL to Power BI. The following
checks and preparation steps were completed:
1. Loaded the project_csat_analytics CSAT table.
2. Reviewed the column names and assigned suitable data types to text,
   numeric, and date fields.
3. Standardized the date separators in call_timestamp.
4. Converted call_timestamp to the Date data type using the English
   (United States) locale.
5. Checked column quality in Power Query. The profile showed 100% valid
   values, with no errors or empty values.
6. Checked for exact duplicate rows across all 13 columns. No exact
   duplicates were found; the row count remained 32,941.
Dashboard Contents
KPI Cards
  KPI                          Displayed value
  Total Calls                           32,941
Average CSAT                            2.07
Average Duration Minutes               25.02
Charts
  Visual                              Purpose
  Daily Call Volume Trends -- October Shows the daily number of calls
2020 (Line chart)                   during October 2020

  Customer Calls by Channel (Doughnut Compares the share of calls by
chart)                              contact channel

  Calls by State -- Map               Displays call volume by state

  Customer Calls by Reason (Column    Compares the main reasons for
chart)                              customer calls
Customer Calls by Response Time     Shows calls in each response-time
(Bar chart)                         category
Slicers
- Call Date
- State
- Sentiment
- Call Channel
The slicers allow the dashboard to be filtered by the selected date,
state, sentiment, and channel.
Key Findings
1. Call volume changed across the month. October 21 showed 1,170
   calls, the highest daily value recorded in the dashboard. October 31
   showed 1 call. This final-day value should be read as the count
   recorded for that date, rather than assumed to represent a normal
   full day.
2. Call-Center was the most-used channel. It represented 32.30% of
   calls. Chatbot accounted for 25.06%, Email for 22.68%, and Web for
   19.96%.
3. Billing Question was the largest call reason. The chart showed
   approximately 23.5K calls for Billing Question and approximately
   4.7K each for Payments and Service Outage. These are rounded
   readings from the dashboard chart.
4. Most calls were in the Within SLA category. The dashboard showed
   20,625 calls, or 62.61%.
5. The other response-time categories contained a sizeable share of
   calls. Below SLA accounted for 8,148 calls (24.74%), while Above
   SLA accounted for 4,168 calls (12.65%). The category names are
   reported as shown in the dataset; their operational meaning should
   follow the project's SLA definition.
6. The map shows substantial call counts in the states checked.
   California showed 3,631 calls, Texas 3,572, and Florida 2,834. These
   are individual values checked on the map and are not presented as a
   confirmed ranking of all states.
Response-Time Values
  Category            Calls         Share
  Within SLA         20,625        62.61%
Below SLA           8,148        24.74%
Above SLA           4,168        12.65%
Total      32,941   100.00%

Percentages are rounded to two decimal places.
Recommendations
1. Reduce billing-related customer issues. Review common billing
   questions, make payment information easier to understand, provide
   clear billing FAQs, and investigate repeated billing complaints.
2. Review response-time performance. Monitor the calls in each SLA
   category, check when response delays occur, and compare staffing
   levels with busy periods. Interpret the categories using the
   project's official SLA definitions.
3. Improve the quality of customer support. Review recurring
   complaints and customer feedback, provide focused agent training,
   and check whether the chatbot and website help customers resolve
   simple questions.
Power BI Dashboard Creation Process
1. Open Power BI Desktop and connect to the MySQL database using the
   project connection details.
2. Select and load the project_csat_analytics CSAT table.
3. Open Power Query and review the column names and data types.
4. Correct the call_timestamp format and convert it to Date.
5. Check column quality and exact duplicate rows.
6. Create KPI cards for Total Calls, Average CSAT, and Average Duration
   Minutes.
7. Add a line chart for daily call volume using call_timestamp.
8. Add a doughnut chart using channel.
9. Add a map using state as the location and call count as the value.
10. Add a column chart using reason.
11. Add a bar chart using response_time.
12. Add slicers for Call Date, State, Sentiment, and Call Channel.
13. Check chart titles, displayed values, and slicer behavior, then save
    the Power BI report.
Conclusion
The dashboard provides a single view of customer support activity across
call trends, contact channels, states, call reasons, and response-time
categories. Billing questions account for the largest visible
call-reason group, while the response-time chart shows how calls are
distributed across the three recorded SLA categories. These results can
help the support team decide which areas to review first.
Project Files
Customer-Satisfaction-Analysis/
|
|-- README.md
|
|-- PowerBI/
|   |-- CSAT_Analytics.pbix
|
|-- Documentation/
|   |-- CSAT_Analytics_Project_Documentation.docx
|   |-- CSAT_Analytics_Project_Documentation.pdf
|
|-- Presentation/
|   |-- CSAT_Analytics_Project_Presentation.pptx
|
|-- Screenshots/
    |-- Customer Satisfaction Dashboard.png
Notes and Limitations
- The analysis covers the records loaded for October 2020 and should
  not be treated as a current view of customer behavior.
- The dashboard screenshot and figures show the values displayed in
  the Power BI report. Approximate call-reason values are identified
  as approximate.
- The three state counts are examples checked individually, not a
  verified ranking of the highest-volume states.
- The SLA category labels are retained as provided. Their precise
  business interpretation depends on the project definition.
- The dashboard provides descriptive analysis; it does not by itself
  establish why customers call or prove that a particular service
  change will improve satisfaction.
- Database credentials and private connection details are not included
  in this repository.
Project: CSAT Analytics
Report: Customer Satisfaction Analysis Dashboard
Tool: Microsoft Power BI
