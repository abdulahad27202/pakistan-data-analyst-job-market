# Pakistan Data Analyst Job Market Analysis

A Power BI dashboard analyzing 60+ live Data Analyst job postings from Rozee.pk, identifying the most in-demand skills and top hiring cities across Pakistan.

## Data Collection

Job listings were originally targeted for automated collection via a Python (Selenium) web scraper. After encountering site-level anti-bot protections that blocked reliable automated access, collection was pivoted to a manual, verified process instead — prioritizing data authenticity over automation. Each listing's title, company, city, posted date, and listed skills were captured and structured into Excel workbooks using **openpyxl**.

## Data Cleaning

Skill tags in the raw listings were inconsistently labeled (for example, "MS Excel," "Excel Skills," and "Excel" all referring to the same tool). These variants were identified and merged into consistent labels using Power Query, and the cleaned results were cross-checked against a manual summary of the same data to confirm accuracy before building the dashboard.

## What's in the Dashboard

- **Headline KPI cards** — total jobs analyzed, top requested skill, distinct city count, and top hiring city, with the top-skill and top-city cards driven by DAX measures so they update automatically if the data changes.
- **Most Requested Skills** — a Top 10 bar chart ranking skills by how many listings mention them.
- **Demand by City** — a Top 10 bar chart ranking cities by job posting volume.
- **Job Listings table** — the full list of postings with title, company, city, and posted date, sorted most recent first.

## Key Findings

- **Excel** is the single most requested skill, appearing in **50% of listings** — ahead of general "Data Analysis" (39%), Data Entry (30%), and Power BI (14%).
- **Lahore** is the top hiring city (17 listings), narrowly ahead of Karachi (15).
- A meaningful share of postings (14 listings) didn't specify a single city, listing "All Cities" instead — reflecting a chunk of remote-friendly or multi-location hiring.

## Tools

Python · openpyxl · Power BI · DAX · Power Query

## Files

- `Job_Listings.xlsx` — structured job posting data
- `summary.txt` — manual verification summary used to cross-check the cleaned dataset
- `Pakistan Data Analyst Job Market Dashboard.pbix` — the full Power BI report
