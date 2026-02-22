# Employee Daily Resource Tracker - Power BI

## 📌 Project Overview
This project solves a common data challenge: transforming static date ranges (Start Date to End Date) into a dynamic daily headcount and resource list.

## 🛠️ The Challenge
Raw data often comes with just a start and end date for an employee's assignment. This makes it difficult to visualize:
- How many people are working on a specific date?
- Who exactly is active on that day?

## 🚀 The Solution (Power Query / M-Language)
I used **Power Query** in Power BI to automate this transformation:

1. **Date Expansion:** Generated a list of dates between the range using: 
   `{Number.From([Start_Date])..Number.From([End_Date])}`
2. **Data Transformation:** Expanded the list into new rows to create a unique record for every active day.
3. **Advanced Grouping:** Used `Text.Combine` to aggregate employee names for each date/department.

