# 🌍 Travel & Tourism Analytics Dashboard

**An interactive Business Intelligence solution built using Microsoft Power BI to explore travel trends, destination preferences, traveler demographics, financial performance, and customer behavior.**

![Power BI](https://img.shields.io/badge/Power%20BI-Analytics-yellow?logo=powerbi)
![DAX](https://img.shields.io/badge/DAX-Measures-blue)
![Status](https://img.shields.io/badge/Project-Completed-success)
![Domain](https://img.shields.io/badge/Domain-Travel%20%26%20Tourism-orange)

---

## 📌 Project Overview

The Travel & Tourism Analytics Dashboard is a multi-page Power BI project developed to transform travel-related data into meaningful business insights.

The dashboard provides an interactive analytical experience through five dedicated report pages, covering destination analysis, traveler demographics, cost analysis, and travel behavior.

It enables users to explore travel patterns, understand customer preferences, analyze expenditure distribution, and monitor important business performance indicators.

## 🎯 Project Objectives

- Identify the most visited travel destinations.
- Analyze traveler demographics and nationality distribution.
- Understand accommodation and transportation preferences.
- Evaluate travel expenditure across different destinations.
- Analyze frequent flyer participation and hotel booking behavior.
- Explore trip duration and travel spending patterns.
- Monitor customer behavior and churn-related indicators.
- Present key business insights through interactive visualizations.

---

# 📊 Dashboard Pages & Features

## 01. Navigation & Overview

**Purpose:** Provide a user-friendly interface for navigating between different analytical report pages.

**Features:**
- Interactive navigation pane.
- Quick switching between dashboard pages.
- Consistent report theme and layout.
- Easy access to different analytical sections.

<img width="706" height="398" alt="01_Navigation_Overview" src="https://github.com/user-attachments/assets/6457035e-a48b-4be8-a73d-f1b50538c3a4" />

## 02. Destination Analysis

**Purpose:** Understand destination popularity, travel preferences, and expenditure patterns.

**Key Metrics & Visualizations:**
- Most Visited Destinations.
- Top Destinations by Travel Expenditure.
- Destination-wise Trip Distribution.
- Accommodation Preferences by Destination.
- Accommodation Spending by Destination.
- Transportation Preferences.
- Destination-wise Cost Comparison.

**Business Questions:**
- Which destinations attract the most travelers?
- Which destinations have the highest travel expenditure?
- What accommodation types are preferred by travelers?
- How does transportation preference vary across destinations?

<img width="705" height="395" alt="02_Destination_Analysis" src="https://github.com/user-attachments/assets/bf356225-75f8-4b06-9997-3d651fa05a69" />

## 03. Traveler Demographics

**Purpose:** Analyze traveler characteristics and understand customer segmentation.

**Key Metrics & Visualizations:**
- Traveler Age Distribution.
- Age Group Segmentation.
- Gender Distribution.
- Nationality-wise Traveler Distribution.
- Frequent Flyer Percentage.
- Frequent Flyer vs. Non-Frequent Flyer Analysis.
- Services Opted by Travelers.
- Traveler Segmentation.

**Business Questions:**
- Which age group travels the most?
- What is the gender distribution?
- Which nationalities are represented in the dataset?
- What percentage of travelers are frequent flyers?
- Which traveler segments show different travel preferences?

<img width="704" height="398" alt="03_Traveler_Demographics" src="https://github.com/user-attachments/assets/f8e567c6-256b-4cfa-a2f5-2f8ce05b2f15" />

## 04. Cost & Financial Analysis

**Purpose:** Evaluate travel expenditure and understand the distribution of costs across different categories.

**Key Metrics & Visualizations:**
- Total Travel Expenditure.
- Accommodation Expenditure.
- Transportation Expenditure.
- Average Trip Cost.
- Destination-wise Travel Expenditure.
- Expenditure by Age Group.
- Accommodation Cost Analysis.
- Transportation Cost Analysis.
- Cost Distribution and Comparison.

**Business Questions:**
- How much is spent on travel overall?
- What proportion of expenditure goes toward accommodation and transportation?
- Which destinations have the highest travel costs?
- How does travel expenditure vary across age groups?
- What is the average cost per trip?

<img width="707" height="398" alt="04_Cost_Analysis" src="https://github.com/user-attachments/assets/13d0ac7e-28fe-4944-af74-1bd8822bea09" />

## 05. Travel Insights & Customer Behaviour

**Purpose:** Present consolidated travel KPIs and explore customer behavior, booking preferences, and trip duration patterns.

**Key Performance Indicators:**
- Frequent Flyer Percentage.
- Hotel Opted Percentage.
- Average Accommodation Cost.
- Average Transportation Cost.
- Minimum and Maximum Trip Cost.
- Customer Churn Rate.

**Visualizations:**
- Trip Duration Distribution – Column Chart.
- Shortest Trip – KPI Card.
- Average Trip Duration – KPI Card.
- Longest Trip – KPI Card.
- Accommodation Booking Behaviour – Funnel Chart.
- Customer Churn Analysis – Gauge Chart.

**Business Questions:**
- What percentage of travelers are frequent flyers?
- How many travelers opt for hotel accommodation?
- What is the average accommodation and transportation expenditure?
- What are the shortest and longest trip durations?
- Which accommodation types are most preferred?
- What proportion of customers are classified as churned?

<img width="704" height="398" alt="05_Travel_Insights" src="https://github.com/user-attachments/assets/a4b7630e-0e48-4bb7-807e-a49a61a36b68" />


---

# 🛠️ Tools & Technologies

| Technology | Purpose |
|---|---|
| Microsoft Power BI | Dashboard development and visualization |
| Power Query | Data cleaning and transformation |
| DAX | Calculated measures and KPIs |
| Microsoft Excel | Dataset preparation |
| Data Visualization | Analytical storytelling |
| Business Intelligence | Business insights and reporting |

---

# 📈 Key Performance Indicators

The dashboard includes the following important KPIs:

| KPI | Description |
|---|---|
| Total Trips | Total number of recorded trips |
| Total Travel Expenditure | Sum of all travel costs |
| Average Trip Cost | Average expenditure per trip |
| Average Trip Duration | Average duration of trips |
| Frequent Flyer % | Percentage of frequent flyers |
| Hotel Opted % | Percentage of travelers opting for hotels |
| Accommodation Cost Avg. | Average accommodation expenditure |
| Transportation Cost Avg. | Average transportation expenditure |
| Minimum Trip Cost | Lowest recorded trip expenditure |
| Maximum Trip Cost | Highest recorded trip expenditure |
| Churn Rate | Percentage of customers classified as churned |

---

# 🧮 DAX Measures

Examples of DAX measures used in the project:

### Total Trips

```dax
Total Trips =
COUNTROWS('Travel Data')
```

### Total Travel Expenditure

```dax
Total Travel Expenditure =
SUM('Travel Data'[Total Cost])
```

### Average Trip Cost

```dax
Average Trip Cost =
AVERAGE('Travel Data'[Total Cost])
```

### Average Trip Duration

```dax
Average Trip Duration =
AVERAGE('Travel Data'[Duration (days)])
```

### Frequent Flyers

```dax
Positive Frequent Flyers =
CALCULATE(
    COUNTROWS('Travel Data'),
    'Travel Data'[FrequentFlyer] = "Yes"
)
```

### Frequent Flyer Percentage

```dax
Frequent Flyer % =
DIVIDE(
    [Positive Frequent Flyers],
    [Total Trips],
    0
)
```

### Hotel Opted Percentage

```dax
Hotel Opted % =
DIVIDE(
    CALCULATE(
        COUNTROWS('Travel Data'),
        'Travel Data'[BookedHotelOrNot] = "Yes"
    ),
    [Total Trips],
    0
)
```

### Accommodation Expenditure

```dax
Accommodation Expenditure =
SUM('Travel Data'[Accommodation cost])
```

### Transportation Expenditure

```dax
Transportation Expenditure =
SUM('Travel Data'[Transportation cost])
```

### Minimum Trip Cost

```dax
Minimum Trip Cost =
MIN('Travel Data'[Total Cost])
```

### Maximum Trip Cost

```dax
Maximum Trip Cost =
MAX('Travel Data'[Total Cost])
```

*Note: Adjust table and column names to match your actual Power BI model. Additional measures can be included in the DAX documentation.*

---

### Key Observations

- Accommodation accounts for approximately 67.9% of total travel expenditure.
- Transportation accounts for approximately 32.1% of total travel expenditure.
- Three out of five travelers booked hotels.
- All five sample records have a FrequentFlyer value of No.
- The average trip duration is 7.4 days.

**Important:** These observations are based only on five sample records and should not be generalized to the wider tourism industry.

---

# 📁 Repository Structure

```text
Travel-Tourism-Analytics/
│
├── Dashboard/
│   ├── Travel_Tourism_Analytics.pbix
│   │
│   └── Screenshots/
│       ├── 01_Navigation_Overview.png
│       ├── 02_Destination_Analysis.png
│       ├── 03_Traveler_Demographics.png
│       ├── 04_Cost_Analysis.png
│       └── 05_Travel_Insights.png
│
├── Dataset/
│   └── Travel_Tourism_Data.xlsx
│
├── DAX/
│   └── Measures.md
│
├── Documentation/
│   └── Project_Documentation.md
│
└── README.md
```

---

# 🚀 Learning Outcomes

Through this project, I explored and demonstrated:

- Development of interactive multi-page Power BI dashboards.
- Data cleaning and transformation using Power Query.
- Creation of calculated measures using DAX.
- Development of analytical KPIs.
- Traveler segmentation and demographic analysis.
- Financial and expenditure analysis.
- Interactive report navigation and data exploration.
- Converting raw data into meaningful business insights.

---

# 👨‍💻 About This Project

This is a personal learning and portfolio project developed to demonstrate practical skills in Data Analytics, Business Intelligence, and Power BI dashboard development.

**Domain:** Travel & Tourism Analytics  
**Tool:** Microsoft Power BI  
**Technologies:** Power Query, DAX, Excel  
**Project Type:** Data Analytics & Business Intelligence

---

⭐ If you find this project interesting, feel free to explore the dashboard and its analytical features.

**Thank you for visiting!**
