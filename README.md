# Washington Crimes Analysis 
# Washington DC Crime Analysis

![Excel](https://img.shields.io/badge/Tool-Microsoft%20Excel-217346?style=flat&logo=microsoft-excel&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-brightgreen)
![Domain](https://img.shields.io/badge/Domain-Public%20Safety%20%7C%20Crime%20Analytics-red)

---

## Table of Contents
1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Objectives](#objectives)
4. [Dataset Description](#dataset-description)
5. [Tools Used](#tools-used)
6. [Data Cleaning Process](#data-cleaning-process)
7. [Data Analysis](#data-analysis)
8. [Dashboard](#dashboard)
9. [Key Insights](#key-insights)
10. [Recommendations](#recommendations)
11. [Limitations](#limitations)
12. [Conclusion](#conclusion)
13. [Project Files](#project-files)
14. [Contact Information](#contact-information)

---

## Project Overview

This project presents a comprehensive crime pattern analysis of Washington DC using Microsoft Excel. The dataset covers 3,866 reported crime incidents spanning January and February 2025, capturing offenses across multiple crime types, locations, time periods, shifts, wards, and neighbourhood clusters.

The aim of this analysis was to identify where crimes are most concentrated, when they tend to occur, what types dominate, and which areas require the most urgent attention — translating raw crime records into actionable insights that can support law enforcement planning, community safety awareness, and crime prevention strategies.

---

## Problem Statement

Washington DC experiences a wide range of criminal activity across its wards, precincts, and neighbourhood clusters. Without a structured analysis of crime patterns, it becomes difficult to determine which locations are most at risk, which offence types are most prevalent, and during which time periods crimes are most likely to occur.

This project addresses that challenge by analyzing reported crime data to uncover patterns and provide data-backed recommendations for improving community safety and supporting informed decision-making by authorities and residents.

---

## Objectives

- Identify the most frequently reported crime types across Washington DC
- Determine which locations, wards, and neighbourhood clusters have the highest crime concentration
- Analyze crime distribution by day of the week and time of day to identify peak periods
- Compare property crime versus violent crime across the dataset
- Deliver actionable recommendations to support crime awareness, theft prevention, and community safety

---

## Dataset Description

The dataset contains **3,866 reported crime incidents** recorded across January and February 2025 in Washington DC. Each record represents a single crime incident and captures detailed information across multiple fields covering the nature of the crime, its location, and the timing of the event.

The **offense-text** and **Offense types** fields describe the specific crime committed — including categories such as Other Theft, Theft from Auto, Auto Theft, Robbery, Burglary, Weapon Assault, Homicide, Sex Abuse, and Arson. The **offensegroup** field classifies each incident as either a property crime or a violent crime, enabling a high-level breakdown of crime nature across the dataset.

Geographic fields including **BLOCK**, **WARD**, **DISTRICT**, **NEIGHBORHOOD_CLUSTER**, **PSA** (Police Service Area), and **VOTING_PRECINCT** allow for granular location-based analysis across Washington DC's administrative and policing zones. Coordinates are also captured through **LATITUDE**, **LONGITUDE**, **XBLOCK**, and **YBLOCK** fields for spatial reference.

Time-based fields include **REPORT_DAT** (the date and time the crime was reported), **START_DATE** and **END_DATE** (the estimated window when the crime occurred), **report date**, and **report day** (the day of the week). The **SHIFT** field categorises incidents into day, evening, and midnight shifts, enabling time-of-day pattern analysis.

Additional administrative fields include **CCN** (the unique crime case number), **OCTO_RECORD_ID**, **ANC** (Advisory Neighbourhood Commission), **CENSUS_TRACT**, **SECTOR**, **BID** (Business Improvement District), **METHOD** (the method used in the offence), and **resolution** (the outcome status of the case).

**Dataset Summary:**
- Total Records: 3,866 crime incidents
- Time Period: January – February 2025
- Crime Categories: Property (3,446) and Violent (420)
- Shifts Covered: Day, Evening, Midnight

---

## Tools Used

- **Microsoft Excel** — Data cleaning, pivot table analysis, and dashboard development
  - PivotTables — for aggregating crime counts by type, location, day, shift, and ward
  - PivotCharts — for visual representation of crime trends and distributions
  - Conditional Formatting — for highlighting hotspot locations and high-frequency patterns
  - Slicers — for interactive filtering on the dashboard
  - Formulas — COUNTIF, calculated fields for KPI tracking

---

## Data Cleaning Process

Before analysis, the dataset was reviewed and prepared to ensure consistency and accuracy:

- **Date and time formatting** — Report dates and start/end times were stored in mixed formats and were standardised to ensure accurate time-based filtering and analysis
- **Column labelling** — Several fields were stored under generic names (Column1, Column2, Column3 etc.) and were reviewed and renamed for clarity during analysis
- **Data type validation** — Numerical and date fields were verified and formatted correctly for use in PivotTables
- **Missing values** — Fields such as END_DATE, BID, and NEIGHBORHOOD_CLUSTER contained blank entries which were reviewed and handled appropriately without distorting the analysis
- **Duplicate checks** — The dataset was screened for duplicate CCN (case number) entries to ensure each record represented a unique incident
- **Offense type standardisation** — Offense labels were reviewed for consistency across the offense-text, offensekey, and Offense types fields to ensure accurate grouping in the analysis

---

## Data Analysis

The analysis was structured across five key dimensions:

**1. Crime Type Distribution**
All offences were grouped and counted to identify the most and least prevalent crime types across the full dataset, distinguishing between property and violent crimes.

**2. Location-Based Analysis**
Crime incidents were aggregated by ward, neighbourhood cluster, and block to identify geographic hotspots with the highest concentration of reported crimes.

**3. Time-of-Day and Day-of-Week Analysis**
Incidents were analysed by shift (day, evening, midnight) and by day of the week to identify peak crime periods and recurring patterns in crime timing.

**4. Property vs. Violent Crime Breakdown**
The offensegroup field was used to compare the volume and distribution of property crimes versus violent crimes across the dataset.

**5. Monthly Trend Analysis**
Crime counts were compared between January (2,033 incidents) and February (1,833 incidents) to assess short-term trends.

---

## Dashboard

The project includes an interactive Excel dashboard built with PivotCharts, slicers, and conditional formatting, providing a visual overview of:

- Crime type distribution across all incident categories
- Top crime hotspot locations and neighbourhood clusters
- Day-of-week and shift-based crime frequency
- Property vs. violent crime breakdown
- Ward-level and precinct-level crime counts

> 📁 Dashboard screenshots are available in the repository files below.

---

## Key Insights

**Crime Type Distribution**
- **Other Theft** was the most reported crime type with **1,610 incidents**, accounting for the largest share of all reported offences
- **Theft from Auto** followed with **897 incidents** and **Auto Theft** with **797 incidents**, making vehicle-related theft a dominant concern
- **Robbery** accounted for **262 violent incidents**, the most common violent offence in the dataset
- **Homicide** was recorded **29 times** and **Sex Abuse 13 times** during the period

**Property vs. Violent Crime**
- Property crimes made up the overwhelming majority at **3,446 incidents (89.1%)** compared to **420 violent crimes (10.9%)**

**Location Hotspots**
- The **3100–3299 block of 14th Street Northwest** was the single most crime-affected location with **63 incidents**
- **500–799 block of Rhode Island Avenue Northeast** recorded **47 incidents**, the second highest
- **Neighbourhood Cluster 2** had the highest crime count among clusters with **290 incidents**, followed by Cluster 23 (264) and Cluster 25 (252)
- **Ward 5** recorded the highest crime volume at **773 incidents**, followed by Ward 3 (666) and Ward 2 (652)

**Time Patterns**
- **Evening shift** had the highest crime occurrence with **1,663 incidents**, followed by the day shift (1,513) and midnight (690)
- **Friday** was the most active crime day with **602 incidents**, closely followed by Tuesday (599) and Wednesday (588)
- **Sunday** had the lowest crime count at **442 incidents**

**Monthly Trend**
- January recorded more crimes (2,033) than February (1,833), suggesting a slight decrease in reported incidents across the two months

---

## Recommendations

1. **Increase evening patrols on 14th Street Northwest and Rhode Island Avenue Northeast** — These locations recorded the highest incident concentrations and should be prioritised for targeted law enforcement presence, particularly during evening hours.

2. **Focus anti-theft campaigns on vehicle-related crimes** — With over 1,694 combined incidents of Theft from Auto and Auto Theft, public awareness campaigns on vehicle security — such as not leaving valuables visible and using steering locks — could have a measurable impact.

3. **Deploy resources strategically on Fridays and evenings** — Crime is consistently highest on Fridays and during the evening shift. Law enforcement scheduling and patrol allocation should reflect these peak periods.

4. **Target Ward 5 and Neighbourhood Clusters 2, 23, and 25 for community engagement** — These areas record disproportionately high crime counts and would benefit from community policing initiatives, neighbourhood watch programmes, and increased social services presence.

5. **Address violent crime in Ward 1 and high-robbery precincts** — Precinct 1 recorded 56 incidents. A focused strategy on robbery prevention — including street lighting improvements and community outreach — could reduce violent crime in key zones.

6. **Monitor the January-to-February trend** — The slight decrease from January to February should be tracked over subsequent months to determine whether it reflects a genuine downward trend or a seasonal variation.

---

## Limitations

- **Short time period** — The dataset only covers January and February 2025, making it difficult to draw conclusions about annual trends, seasonal patterns, or long-term changes in crime rates
- **No demographic data** — The dataset does not include information about victims or perpetrators, limiting the depth of social or community-based analysis
- **Reporting bias** — Not all crimes are reported to authorities, meaning the dataset likely underrepresents the true volume of incidents, particularly for less severe offences
- **Resolution data incomplete** — The resolution field, which captures whether a case was closed or resulted in an arrest, had inconsistent or missing values for many records, limiting case outcome analysis
- **No socioeconomic context** — The analysis does not account for underlying socioeconomic factors such as poverty rates, unemployment, or housing density, which are often closely linked to crime patterns

---

## Conclusion

This analysis of Washington DC crime data revealed clear patterns in the type, location, and timing of criminal activity across the city. Property crimes — particularly theft — dominate the landscape, with 14th Street Northwest and Rhode Island Avenue Northeast emerging as key hotspot locations. Evening hours and Fridays are consistently the highest-risk periods, and Ward 5 and Neighbourhood Clusters 2, 23, and 25 carry the heaviest crime burden.

The insights from this analysis provide a data-driven foundation for law enforcement agencies, community organisations, and city planners to make more targeted decisions around patrol deployment, public safety campaigns, and community investment — ultimately supporting a safer Washington DC.

---

## Project Files

| File | Description |
|---|---|
| `Washington_Crime_Analysis.xlsx` | Main Excel workbook containing raw data, analysis sheets, and dashboard |

---

## Contact Information

**Aladeloye Esther Aderonke**
Data & Business Analyst | Healthcare · Business · Finance

- 📧 Email: aladeloyeesther616@gmail.com
- 💼 LinkedIn: [linkedin.com/in/estheraderonke](https://linkedin.com/in/estheraderonke)
- 🐙 GitHub: [github.com/aderonke27](https://github.com/aderonke27)
- 📱 Phone: +234 810 636 6936

---

*This project was completed as part of a data analytics portfolio demonstrating crime data analysis, pattern recognition, and data-driven community safety recommendations.*

## Table of Contents
1. [Project Overview](#project-overview)
2. [Problem Statement](#problem-statement)
3. [Objectives](#objectives)
4. [Dataset Description](#dataset-description)
5. [Tools Used](#tools-used)
6. [Data Cleaning Process](#data-cleaning-process)
7. [Data Analysis](#data-analysis)
8. [Dashboard](#dashboard)
9. [Key Insights](#key-insights)
10. [Recommendations](#recommendations)
11. [Limitations](#limitations)
12. [Conclusion](#conclusion)
13. [Project Files](#project-files)
14. [Contact Information](#contact-information)

## Project Overview
Crime incidents continue to pose threats for urban safety and effective law enforcement resource allocation. This project focuses on analyzing reported crime data to identify patterns, trends, and key areas of concern in Washington. Using Microsoft Excel, a crime analysis dashboard was created to transform raw crime data into insights that can help better understand the distribution of crimes across different locations, time periods, and offense categories.

The analysis was conducted to address the need for clearer visibility into crime patterns within the dataset, which recorded 3,866 reported incidents over a two-month period. By examining crime types, districts, shifts, days of the week, and specific locations, the project aims to highlight crime hotspots and identify when crimes are most likely to occur. Understanding these patterns can support data-driven decision-making for crime prevention and resource allocation.

The dashboard provides a visual summary of crime trends, including crime distribution by offense group, crime by district, crime by shift, monthly crime trends, and location hotspots. Through these visualizations, the dashboard enables stakeholders to quickly identify high-risk areas, dominant crime types, and peak crime periods, ultimately supporting strategies aimed at improving public safety and reducing crime incidents.

## Problem Statement
Despite the availability of crime data, there is limited clarity on where crimes occur most frequently, when they are most likely to happen, and which crime types dominate in Washington. With 3,866 reported incidents within two months, authorities and stakeholders need a clear understanding of crime patterns across locations, time periods, and offense categories to support effective resource allocation and crime prevention strategies.

## Objectives
* Analyze the overall crime volume to understand the scale of reported crimes within the study period.
* Identify the most common crime types to determine which offenses contribute most to the total crime rate.
* Locate crime hotspots by identifying blocks or areas with the highest number of reported crimes.
* Examine crime distribution by offense group to compare property crimes with violent crimes.
* Analyze crime patterns across different shifts (day, evening, midnight) to determine peak crime periods.
* Evaluate monthly crime trends to observe whether crime rates are increasing or decreasing over time.
* Assess crime occurrence by day of the week to determine the days with the highest and lowest crime activity.
* Identify districts with the highest crime levels to highlight areas that may require targeted intervention.

## Dataset Description

## Tools Used
Microsoft Excel

## Data Cleaning Process

## Data Analysis

## Dashboard
<img width="1564" height="795" alt="Screenshot (184)" src="https://github.com/user-attachments/assets/bf2fa2d8-a98c-4415-86b0-1b03ca6c0a57" />

## Key Insights
* A total of 3,866 crimes were reported during the analyzed period, indicating a high level of criminal activity.
* Other Theft is the most reported crime with 1,610 cases.
* The 3100 – 3299 block of 14th Street Northwest emerged as the primary crime hotspot with the highest number of reported incidents.
* Evening shift records the highest crime occurrence with 1,663 cases, followed by daytime shift.
* Property crimes (3,446) significantly outnumber violent crimes (420).
* Fridays have the highest number of crime reports with 602 cases, while Sundays have the lowest number of reported crimes with 442 cases.
* January recorded 2,033 crimes while February recorded 1,833, showing a small deline in reported incidents.
* District 5 (773 cases) reports the highest crime rate among all districts, making it the most affected district.

## Recommendations
* Increase security and surveillance in identified hotspots, particularly around the 3100–3299 block of 14th Street Northwest, through increased police patrols, CCTV installation, and improved street lighting to deter criminal activity.
* Prioritize theft prevention strategies since Other Theft, Theft from Auto, and Auto Theft account for the majority of crimes. Public awareness campaigns, vehicle security initiatives, and stronger monitoring of parking areas can help reduce these incidents.
* Allocate more law enforcement resources during evening hours, as the evening shift records the highest number of crimes. Strategic patrol scheduling can help reduce crime during peak periods.
* Implement targeted policing in high-crime districts, particularly District 5, District 3, and District 2, which report the highest crime volumes. This may include community policing and focused patrol operations.
* Strengthen crime prevention measures toward the end of the week, especially on Fridays, when crime occurrences peak. Increasing patrol visibility during these periods may deter potential offenders.
* Enhance community engagement programs in high-crime areas to encourage residents to report suspicious activities and collaborate with law enforcement to improve neighborhood safety.
* Monitor and evaluate monthly crime trends regularly to determine whether implemented crime reduction strategies are effective and to adjust interventions where necessary.
* Develop data-driven decision-making systems, such as crime dashboards and predictive analytics, to help law enforcement agencies continuously track crime patterns and respond proactively.
* Promote situational crime prevention strategies, such as better urban planning, improved lighting, controlled access to vulnerable areas, and public awareness programs to reduce opportunities for property crimes.

## Limitations
* Limited time frame of the data: The analysis only covers two months (January and February), which may not fully represent long-term crime trends or seasonal variations.
* Possible underreporting of crimes: The dataset only includes reported crimes, meaning incidents that were not reported to authorities are not captured in the analysis.
* Lack of demographic and socio-economic data: The dataset does not include information such as population density, income levels, or age groups, which could help explain underlying causes of crime patterns.
* Absence of detailed location context: Although the analysis identifies hotspots, it does not provide deeper context such as business activity, nightlife areas, or residential density that may influence crime rates.
* Limited crime categorization: Some crimes are grouped under broad categories like “Other Theft,” which makes it difficult to understand the specific types of theft occurring.
* Data quality issues: The presence of “Unknown” districts suggests some records may have incomplete or missing location data.
* No information on law enforcement response: The dataset does not include data on police response times, arrests, or case outcomes, which limits deeper evaluation of crime control effectiveness.
* No historical comparison: Without data from previous years, it is difficult to determine whether crime levels are improving, worsening, or remaining stable.

## Conclusion

## Project Files

## Contact Information
LinkedIn: https://www.linkedin.com/in/estheraderonke

Email: aladeloyeesther616@gmail.com
