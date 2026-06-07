# Washington Crimes Analysis

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
The dataset contains 3,866 reported crime incidents recorded across January and February 2025 in Washington DC. Each record represents a single crime incident and captures detailed information across multiple fields covering the nature of the crime, its location, and the timing of the event.

The offense-text and Offense types fields describe the specific crime committed, covering categories such as Other Theft, Theft from Auto, Auto Theft, Robbery, Burglary, Weapon Assault, Homicide, Sex Abuse, and Arson. The offensegroup field classifies each incident as either a property crime or a violent crime, enabling a high-level breakdown of crime nature across the dataset. Of the 3,866 incidents recorded, 3,446 were property crimes and 420 were violent crimes.

Location is captured across several geographic fields. The BLOCK, WARD, DISTRICT, NEIGHBORHOOD_CLUSTER, and PSA (Police Service Area) fields allow for granular location-based analysis across Washington DC's administrative and policing zones, while the VOTING_PRECINCT field adds an additional layer of geographic segmentation. Spatial coordinates are also recorded through the LATITUDE, LONGITUDE, XBLOCK, and YBLOCK fields for map-based reference.

On the time side, REPORT_DAT captures the exact date and time each crime was reported, while START_DATE and END_DATE record the estimated window during which the incident occurred. The report date and report day fields enable day-of-week analysis, and the SHIFT field categorises each incident into one of three time periods — day, evening, or midnight — supporting time-of-day pattern analysis across the dataset.

Several additional administrative fields are also included. The CCN field provides a unique case number for each incident, while OCTO_RECORD_ID serves as a system identifier. The ANC (Advisory Neighbourhood Commission), CENSUS_TRACT, SECTOR, and BID (Business Improvement District) fields add further geographic and administrative context. The METHOD field records how the offence was carried out, and the resolution field captures the outcome status of each case.

## Tools Used
Microsoft Excel

## Data Cleaning Process
Before analysis, the dataset was reviewed and prepared to ensure consistency and accuracy:
* Date and time formatting — Report dates and start/end times were stored in mixed formats and were standardised to ensure accurate time-based filtering and analysis
* Column labelling — Several fields were stored under generic names (Column1, Column2, Column3 etc.) and were reviewed and renamed for clarity during analysis
* Data type validation — Numerical and date fields were verified and formatted correctly for use in PivotTables
* Missing values — Fields such as END_DATE, BID, and NEIGHBORHOOD_CLUSTER contained blank entries which were reviewed and handled appropriately without distorting the analysis
* Duplicate checks — The dataset was screened for duplicate CCN (case number) entries to ensure each record represented a unique incident
* Offense type standardisation — Offense labels were reviewed for consistency across the offense-text, offensekey, and Offense types fields to ensure accurate grouping in the analysis

## Data Analysis
The analysis was structured across five key dimensions:
* Crime Type Distribution: All offences were grouped and counted to identify the most and least prevalent crime types across the full dataset, distinguishing between property and violent crimes.
* Location-Based Analysis: Crime incidents were aggregated by ward, neighbourhood cluster, and block to identify geographic hotspots with the highest concentration of reported crimes.
* Time-of-Day and Day-of-Week Analysis: Incidents were analysed by shift (day, evening, midnight) and by day of the week to identify peak crime periods and recurring patterns in crime timing.
* Property vs. Violent Crime Breakdown: The offensegroup field was used to compare the volume and distribution of property crimes versus violent crimes across the dataset.
* Monthly Trend Analysis: Crime counts were compared between January (2,033 incidents) and February (1,833 incidents) to assess short-term trends.

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
This analysis of Washington DC crime data revealed clear patterns in the type, location, and timing of criminal activity across the city. Property crimes — particularly theft — dominate the landscape, with 14th Street Northwest and Rhode Island Avenue Northeast emerging as key hotspot locations. Evening hours and Fridays are consistently the highest-risk periods, and Ward 5 and Neighbourhood Clusters 2, 23, and 25 carry the heaviest crime burden.

The insights from this analysis provide a data-driven foundation for law enforcement agencies, community organisations, and city planners to make more targeted decisions around patrol deployment, public safety campaigns, and community investment — ultimately supporting a safer Washington DC.

## Project Files
[Veiw main Excel Workbook](./Washington_Crimes_Overveiw.xlsx)

The Excel workbook contains the raw dataset, analysis sheet, and the dashboard

## Contact Information
* LinkedIn: https://www.linkedin.com/in/estheraderonke
* Email: aladeloyeesther616@gmail.com
