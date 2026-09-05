Cyclistic Bike-Share Analysis

Google Data Analytics Professional Certificate — Capstone Project

Overview

In this case study, I analyzed twelve months of trip data from Cyclistic, a Chicago-based bike-share company, to understand how annual members and casual riders use the service differently. The business goal was to support Cyclistic's marketing team in designing a campaign to convert casual riders into annual members, who are more profitable for the company.

Business Task

Design marketing strategies aimed at converting casual riders into annual members by first understanding how the two groups differ in their bike usage.

Data & Tools
Source: Twelve months of Cyclistic trip data (~6.04 million rides), one row per ride, including bike type, start/end timestamps, start/end station, and rider type (casual or member).
Tools: Python (pandas) in Google Colab for cleaning and analysis at scale, and Google Sheets for building the final summary dashboard and charts.
Process

The raw data required two significant fixes before it could be trusted:

A mixed date format in the timestamp columns was distorting monthly totals, at one point making July, a peak summer month, look almost empty.
A batch of corrupted duplicate columns (misspelled leftovers from a broken earlier calculation, e.g. ride_lenght, day_of_teh_week) had to be dropped and recalculated directly from the timestamps.

Rides under 1 minute or over 24 hours (likely false starts, or lost/stolen bikes) were filtered out as a standard industry convention. After cleaning, the dataset went from 6,037,968 to 5,871,696 valid rides (2.75% removed).

Key Findings
Seasonality: Both rider types peak in summer and drop in winter, but casual ridership swings far more dramatically between the two.
Day of week: Friday and Saturday are consistently the busiest days system-wide.
Ride duration: Casual riders ride longer than members in every single month of the year, with the widest gap in summer.
Station usage: The ten most popular stations cluster along the lakefront and downtown tourist corridor (Navy Pier, Millennium Park, and similar).
Bike type: Electric bikes make up roughly two-thirds of rides for both groups, though classic bikes average a longer ride time.
Recommendations
Time membership acquisition campaigns for the spring shoulder season, ahead of the summer casual-ridership peak.
Geo-target advertising at the specific lakefront and tourist stations where casual riders concentrate.
Test a lower-cost, weekend-focused membership tier.
Lead marketing messages with the cost savings of a membership versus per-ride pricing for longer trips.
Pair classic-bike, scenic-route promotion with membership upsells.
Repository Contents
File	Description
Cyclistic_Capstone_Report.docx / .pdf	Final executive report: business task, methodology, key findings, and recommendations.
Cyclistic_Case_Study_QA.docx / .pdf	Answers to the official 26 guiding questions across all six phases of the data analysis process (Ask, Prepare, Process, Analyze, Share, Act).
Cyclistic_Analysis_Notebook.ipynb	Python/pandas notebook with the full data cleaning and analysis process.
dashboard_screenshots/	Screenshots of the final six-chart dashboard built in Google Sheets.
About This Project

This was my first end-to-end data analytics project, completed as the capstone for the Google Data Analytics Professional Certificate. It covers the full analytics process: asking the right business question, preparing and auditing the data, cleaning and processing it programmatically, analyzing it for patterns, and communicating findings through visualizations and a written report aimed at a non-technical, executive audience
