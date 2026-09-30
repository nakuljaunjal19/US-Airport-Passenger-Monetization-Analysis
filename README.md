# ✈️ U.S. Airport Passenger Monetization & Financial Analysis

A data analysis project examining how major U.S. airports convert passenger traffic into commercial revenue and how their financial performance compares with peer airports.

The project analyzes **31 U.S. Large Hub airports from 2019–2024** using FAA airport financial data. It combines data preparation, dimensional modeling, DAX measures, peer benchmarking, and interactive Power BI dashboards to identify differences in passenger monetization and commercial revenue performance.

## 🛠️ Tools & Technologies

- Power BI
- Power Query
- DAX
- Excel
- Data Modeling
- Data Visualization
- Financial & Business Analysis

## 📊 Dashboard Overview

![Airport Financial Performance Dashboard](dashboard/overview.png)

## Business Problem

Major U.S. airports can handle similar passenger volumes but still generate very different levels of revenue.

The goal of this project was to understand how well airports are converting passenger traffic into revenue, compare their performance with other large airports, and identify which commercial revenue categories are contributing to the differences.

## What I Did

I cleaned and prepared financial and passenger data for 31 large U.S. airports covering 2019 to 2024.

I then built a Power BI data model and created measures to analyze:

- Revenue per passenger
- Commercial revenue per passenger
- Operating margin
- Passenger and revenue growth
- Peer median performance
- Airport monetization ranking
- Commercial revenue performance by category

The dashboard is split into two pages. The first page looks at overall financial and passenger performance, while the second page focuses more closely on passenger monetization and peer comparison.

## Monetization Analysis

The second page focuses on how much commercial revenue airports generate from their passenger traffic.

It allows an airport to be compared with the peer median and shows which commercial revenue categories are performing above or below the benchmark.

![Airport Monetization Dashboard](dashboard/Monetization.png)


## Key Findings

- Across the 31 airports, passenger traffic reached about **716.2 million enplanements in 2024**, around **4.7% higher than 2019**. Over the same period, operating revenue increased by about **30%**, from $17.46B to $22.69B.

- **Revenue per passenger increased from $25.53 in 2019 to $31.68 in 2024**, an increase of about **24%**. Known commercial revenue per passenger also increased from **$8.82 to $10.71**.

- **Boston Logan (BOS)** had the highest known commercial revenue per passenger in 2024 at **$18.72**, compared with the peer median of **$11.26**. This was about **66% above the peer median**.

- Passenger volume alone did not determine monetization performance. **Atlanta (ATL)** had the highest passenger volume at about **53.7M enplanements**, but generated only **$6.72 in known commercial revenue per passenger**, around **40% below the peer median**.

- **Los Angeles (LAX) and Chicago O'Hare (ORD)** handled relatively similar passenger volumes in 2024 — about **38.3M and 40.0M enplanements** — but LAX generated **$13.36 in known commercial revenue per passenger compared with $7.34 at ORD**.

- **Parking & Ground Transportation** was the largest known commercial revenue category in 2024, generating about **$4.08B** and accounting for roughly **53% of the five known commercial revenue categories**. Rental Car revenue was the second-largest category at about **18%**.

- Total revenue per passenger and commercial monetization did not always move together. **JFK had the highest total operating revenue per passenger at $60.02**, but its known commercial revenue per passenger was only **$7.13**, ranking near the bottom of the 31-airport group.


## Data

The analysis uses FAA airport financial and passenger data for 31 large U.S. airports from 2019 to 2024.

The cleaned dataset includes airport-level information such as:

- Passenger enplanements
- Operating revenue
- Operating expenses
- Operating income
- Capital expenditure
- Commercial revenue by category
- Airport and location details

The commercial revenue analysis currently focuses on five verified categories:

- Parking & Ground Transportation
- Rental Car
- Food & Beverage
- Retail
- Terminal Services

## Data Model

I used a dimensional model in Power BI with separate fact and dimension tables.

The model includes:

- Airport dimension
- Year dimension
- Revenue category dimension
- Geography dimension
- Data quality dimension
- Airport performance fact table
- Commercial revenue fact table

![Power BI Data Model](model/model.png)


## Analysis & Measures

I created DAX measures to track financial performance, passenger trends, and airport monetization.

Some of the main measures used in the analysis are:

- Total Operating Revenue
- Total Enplanements
- Revenue per Passenger
- Known Commercial Revenue per Passenger
- Operating Margin %
- Revenue YoY Growth %
- Passenger YoY Growth %
- Peer Median Revenue per Passenger
- Peer Gap %
- Airport Monetization Rank
- Commercial Revenue Share %
- Category Gap vs Peer Median

The peer comparison measures were designed so that a selected airport can be compared with the rest of the airport group while keeping the selected year and revenue category filters.


## Data Limitations

The FAA source data does not provide complete values for every commercial revenue field used in the original reporting structure.

Because of this, the project uses **Known Commercial Revenue**, which is calculated from five verified categories:

- Parking & Ground Transportation
- Rental Car
- Food & Beverage
- Retail
- Terminal Services

The results should therefore be interpreted as an analysis of these known commercial revenue categories rather than total non-aeronautical revenue.

Peer comparisons also show differences in performance, but they do not by themselves explain the reason for those differences. Factors such as airport size, passenger mix, concession agreements, transportation access, and local market conditions can also affect revenue performance.


## Project Files

- [Power BI Report](powerbi/US_Airport_Passenger_Monetization_Analysis.pbix)
- [Cleaned Dataset](data/Airport_Revenue.xlsx)
- [Overview Dashboard](dashboard/overview.png)
- [Monetization Dashboard](dashboard/Monetization.png)
- [Data Model](model/model.png)
