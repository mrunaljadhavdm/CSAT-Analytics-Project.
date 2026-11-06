# Customer Satisfaction Analysis

**Tools:** MySQL · Microsoft Power BI · Power Query  
**Domain:** Customer Support and Customer Satisfaction Analytics  
**Project Type:** Descriptive Data Analytics  
**Project:** DataMites Capstone 1 – PRDA-02: CSAT Analytics

![Customer Satisfaction Dashboard](Screenshots/Customer%20Satisfaction%20Dashboard.png)

## 1. Business Problem

Customer support teams receive calls through different channels and for different reasons. To improve the support experience, a business needs to understand how many calls it receives, which channels customers use, what issues they report, and how calls are distributed across response-time categories.

This project uses the available CSAT records to bring those details together in one Power BI dashboard.

The dashboard helps answer questions such as:

- How does daily call volume change during the month?
- Which contact channel is used most often?
- Which states account for customer calls?
- What are the main reasons customers contact support?
- How are calls distributed across the recorded response-time categories?
- What is the average CSAT score and average call duration?

## 2. Dataset

The project uses the `project_csat_analytics CSAT` table from the provided MySQL database.

| Dataset Detail | Value |
|---|---:|
| Records loaded into Power BI | 32,941 |
| Columns loaded | 13 |
| Reporting period | October 2020 |
| Main subject | Customer support call records |

The fields include customer and call details such as `id`, `customer_name`, `sentiment`, `csat_score`, `call_timestamp`, `Call_Day`, `reason`, `city`, `state`, `channel`, `response_time`, `call_duration_in_minutes`, and `call_center`.

**Dataset Count Note:** The assignment description referred to 32,942 rows and 12 columns. The connected table in Power BI contained 32,941 rows and 13 columns. The analysis in this project uses the data actually loaded.

## 3. Tools and Methodology

### MySQL

- Used as the source database for the CSAT records.
- Connected the project table to Power BI using the provided database connection details.

### Power Query

- Reviewed column names and data types.
- Standardized the separators in `call_timestamp`.
- Converted `call_timestamp` to the Date data type using the English (United States) locale.
- Checked column quality and exact duplicate rows.

### Power BI

- Created KPI cards for Total Calls, Average CSAT, and Average Duration.
- Built the required charts for call trends, channels, states, call reasons, and response-time categories.
- Added slicers so the report can be filtered by date, state, sentiment, and channel.

## 4. Data Preparation and Validation

The following checks were completed before building the dashboard:

1. Connected Power BI to the MySQL database and loaded the CSAT table.
2. Reviewed the available columns and checked the assigned data types.
3. Corrected the mixed date separators in `call_timestamp` and converted the field to Date.
4. Checked column quality in Power Query. All columns showed 100% valid values, with no errors or empty values.
5. Checked for exact duplicate rows across all 13 columns. No exact duplicates were found, and the row count remained 32,941.

## 5. Key Results and Findings

The values below are taken from the Power BI dashboard and the project checks.

### Main KPIs

| KPI | Dashboard Value |
|---|---:|
| Total Calls | **32,941** |
| Average CSAT | **2.07** |
| Average Call Duration | **25.02 minutes** |

### Call Channel Distribution

| Channel | Share of Calls |
|---|---:|
| Call-Center | **32.30%** |
| Chatbot | **25.06%** |
| Email | **22.68%** |
| Web | **19.96%** |

### Response-Time Categories

| Category | Calls | Share |
|---|---:|---:|
| Within SLA | **20,625** | **62.61%** |
| Below SLA | **8,148** | **24.74%** |
| Above SLA | **4,168** | **12.65%** |
| **Total** | **32,941** | **100.00%** |

Percentages are rounded to two decimal places.

### What the Results Show

1. **Call volume changed during October.** October 21 had the highest daily count shown in the dashboard, with 1,170 calls. October 31 showed 1 call. The final-day value should be checked in the context of the available records and should not automatically be treated as a normal full day.
2. **Call-Center was the most-used channel.** It accounted for 32.30% of calls. Web had the smallest share at 19.96%, while Chatbot and Email accounted for 25.06% and 22.68%.
3. **Billing Question was the largest call reason.** The chart showed approximately 23.5K calls for Billing Question, compared with approximately 4.7K each for Payments and Service Outage. These are rounded chart readings.
4. **Most calls were recorded as Within SLA.** This category contained 20,625 calls, or 62.61% of the total.
5. **The other response-time categories also account for a notable number of calls.** Below SLA contained 8,148 calls (24.74%), and Above SLA contained 4,168 calls (12.65%). The category labels are reported as shown in the dataset; their exact operational meaning should follow the project's SLA definition.
6. **The map provides state-level call counts.** The values checked were California (3,631), Texas (3,572), and Florida (2,834). These are individual map checks, not a confirmed ranking of all states.

## 6. Power BI Dashboard

The report brings the main CSAT measures and call patterns together on one page.

### KPI Cards

- Total Calls
- Average CSAT
- Average Duration Minutes

### Charts

- **Daily Call Volume Trends – October 2020:** Line chart showing calls by date.
- **Customer Calls by Channel:** Doughnut chart showing the share of calls by channel.
- **Calls by State – Map:** Map showing call volume by state.
- **Customer Calls by Reason:** Column chart comparing call reasons.
- **Customer Calls by Response Time:** Bar chart comparing the response-time categories.

### Slicers

- Call Date
- State
- Sentiment
- Call Channel

The slicers allow the dashboard to be filtered using the available date, state, sentiment, and channel values.

## 7. Business Recommendations

These suggestions are based on the patterns visible in the dashboard. They are areas for the support team to review, rather than guaranteed outcomes.

1. **Review billing-related questions.** Billing Question is the largest reason shown in the chart. Review common billing queries, make payment information easier to understand, and provide clear answers to frequently asked questions.
2. **Monitor response-time performance.** Review the number of calls in each response-time category and check when response delays occur. Use the project's SLA definition when deciding which category needs attention.
3. **Improve the support experience.** Review customer feedback and recurring issues, support agents with relevant training, and check whether the chatbot and website help customers resolve straightforward questions.

## 8. Dashboard Creation Process

1. Open Power BI Desktop and connect to the provided MySQL database.
2. Select and load the `project_csat_analytics CSAT` table.
3. Open Power Query and review the column names and data types.
4. Standardize the `call_timestamp` values and convert the field to Date.
5. Check column quality and exact duplicate rows.
6. Create KPI cards for Total Calls, Average CSAT, and Average Duration.
7. Add a line chart using `call_timestamp` and call count to show daily call trends.
8. Add a doughnut chart using `channel` and call count.
9. Add a map using `state` as the location and call count as the value.
10. Add a column chart using `reason` and call count.
11. Add a bar chart using `response_time` and call count.
12. Add slicers for Call Date, State, Sentiment, and Call Channel.
13. Review the chart titles, displayed values, and slicer behavior, then save the Power BI report.

## 9. Conclusion

This project brings together customer call volume, contact channels, state-level call activity, reasons for calling, and response-time categories in one Power BI dashboard. The results show that Billing Question is the largest call-reason group and that Call-Center is the most-used contact channel. The dashboard gives the support team a clear starting point for reviewing billing queries, response-time performance, and the overall customer support experience.

## 10. Limitations and Notes

- The analysis covers the records loaded for October 2020 and should not be treated as a current view of customer behavior.
- The call-reason figures are approximate readings from the dashboard chart.
- The state figures listed are individual values checked on the map and are not a verified top-state ranking.
- The meaning of Below SLA and Above SLA should be confirmed using the project's official SLA definition before making operational conclusions.
- The October 31 count is shown as recorded in the dashboard; the available screenshot alone does not establish whether it represents a complete day.
- The dashboard provides descriptive results. It does not establish why customers contact support or prove that a particular change will improve CSAT.
- Database passwords and private connection details should not be included in the repository.

## 11. Repository Structure

```text
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
```

## Project Summary

**Project:** DataMites Capstone 1 – PRDA-02: CSAT Analytics  
**Report:** Customer Satisfaction Analysis Dashboard  
**Database:** MySQL  
**Visualization:** Microsoft Power BI
