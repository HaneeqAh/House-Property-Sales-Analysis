# House Property Sales Analysis

## Overview
The retail and real estate industries increasingly rely on data analytics tools to estimate property values and understand market behavior. This project focuses on analyzing house property sales in a city in Australia using SQL to uncover insights related to pricing, market trends, geographic variations, and sales performance.

The analysis aims to identify the factors that influence property prices and evaluate the overall health of the real estate market.

---

# Dataset Description

The dataset contains information related to property sales and includes the following columns:

| Column Name | Description |
|-------------|-------------|
| `DateSold` | The date when the property was sold |
| `Postcode` | 4-digit postcode of the suburb where the property was sold |
| `PropertyType` | Type of property (`House` or `Unit`) |
| `Price` | Sale price of the property |
| `Bedrooms` | Number of bedrooms in the property |

---

# Problem Statement

This data analytics project aims to analyze and derive insights from the property sales dataset to better understand the factors influencing property prices and explore trends in the real estate market.

---

# Objectives

## 1. Price Determinants
Identify the major factors influencing property prices, including:

- Location
- Property type
- Number of bedrooms

## 2. Market Trends
Analyze trends in property sales over time to understand how the market has evolved.

## 3. Geographic Variation
Explore variations in property prices across different postcodes and neighborhoods.

## 4. Bedroom Analysis
Investigate the impact of the number of bedrooms on property prices and buyer demand.

## 5. Market Performance
Evaluate the overall performance and condition of the real estate market based on sales data.

---

# Key Questions

The analysis seeks to answer the following business questions:

1. What are the main factors contributing to variations in property prices?
2. Does the number of bedrooms significantly affect property prices?
3. How has the average property price changed over time?
4. Are there seasonal patterns or long-term trends in the market?
5. Is there a correlation between property prices and property type?
6. Are there significant differences in prices across postcodes?
7. Which are the top six postcodes by yearly property price?
8. Which neighborhoods or postcodes show consistent growth in property prices?
9. Which date recorded the highest number of sales?
10. Which year witnessed the lowest number of sales?
11. Which postcode has the highest average price per sale?
12. Are there noticeable patterns in the dates of property sales?
13. What does the sales data reveal about the health of the real estate market?
14. Can potential investment opportunities be identified from the analysis?

---

# Assumptions

The following assumptions were considered during the analysis:

- Currency values remained stable throughout the analysis period.
- Market conditions were relatively stable without major economic disruptions.
- The market is assumed to be homogeneous within each postcode area.
- All significant variables affecting property prices are included in the dataset.
- External factors such as market sentiment and economic changes are not considered.
- Changes in property prices are accurately reflected in the dataset without delay.

---

# Tools & Technologies

The following tools and techniques were used in this project:

- SQL
- Data Cleaning
- Data Aggregation
- Filtering & Grouping
- Window Functions
- Trend Analysis
- Descriptive Analytics

---

# Expected Outcomes

This analysis is expected to provide insights into:

- Property pricing behavior
- High-performing postcodes
- Market growth trends
- Buyer demand patterns
- Seasonal sales activity
- Potential investment hotspots

---

# Project Structure

```bash
House-Property-Sales-Analysis/
│
├── Dataset/
│   └── raw_sales.csv
│
├── SQL Queries/
│   ├── data_cleaning.sql
│   ├── exploratory_analysis.sql
│   └── business_questions.sql
│
├── README.md
│
└── Results/
    └── insights_summary.sql
```

---

# Sample SQL Analysis

## Average Property Price by Property Type

```sql
SELECT 
    PropertyType,
    ROUND(AVG(Price), 2) AS AveragePrice
FROM house_sales
GROUP BY PropertyType;
```

## Top 6 Postcodes by Average Price

```sql
SELECT 
    Postcode,
    ROUND(AVG(Price), 2) AS AveragePrice
FROM house_sales
GROUP BY Postcode
ORDER BY AveragePrice DESC
LIMIT 6;
```

## Year with Lowest Number of Sales

```sql
SELECT 
    EXTRACT(YEAR FROM DateSold) AS Year,
    COUNT(*) AS TotalSales
FROM house_sales
GROUP BY Year
ORDER BY TotalSales ASC
LIMIT 1;
```

---

# Conclusion

This project provides a comprehensive analysis of property sales data to better understand the Australian real estate market. By analyzing pricing patterns, location-based trends, and sales activity, the project supports data-driven decision-making for investors, analysts, and real estate professionals.

---

# Author

**Haneeq**
