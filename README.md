

#Noodles Crypto Analytics Platform



Dashboard screenshot: Docs/screenshots/executive-dashboard.png



\## Project Overview



An end-to-end cryptocurrency social engagement analytics platform developed using Python, MySQL, and Power BI as part of the MVP Studio internship programme.



The platform processes 6,902 social engagement records to provide insights into cryptocurrency engagement, platform performance, and social media trends.



\### Key Features



\- Python-based ETL pipeline using Jupyter notebooks

\- JSON data extraction, cleaning, and transformation

\- Star schema data warehouse design

\- Pre-aggregated reporting tables and SQL views

\- Interactive Power BI reports

\- Data quality and referential integrity validation

\- Manual data refresh with future automation capability



\## Architecture



JSON Files → Python ETL → MySQL (noodles\_dw) → Aggregation Tables and SQL Views → Power BI Dashboards



Architecture diagram:

Docs/architecture-diagram.png



\## Technology Stack



| Layer | Technology |

|---|---|

| Data Sources | JSON, CSV |

| ETL | Python, pandas, SQLAlchemy |

| Development Environment | Jupyter Notebook |

| Data Warehouse | MySQL |

| Database Management | MySQL Workbench |

| Connectivity | MySQL / ODBC |

| Visualization | Power BI Desktop, DAX |

| Version Control | Git, GitHub |



\## Project Structure



```text

noodles-analytics/

├── 05\_data\_warehouse\_design.ipynb

├── 06\_powerbi\_prep.ipynb

├── Reports/

│   ├── NoodlesCrypto\_TopPerformers.pbix

│   └── NoodlesCrypto\_ExecutiveDashboard.pbix

├── Docs/

│   ├── architecture-diagram.png

│   ├── data-dictionary.xlsx

│   ├── technical-runbook.md

│   ├── user-guide.md

│   ├── demo-presentation.pptx

│   └── screenshots/

│       └── executive-dashboard.png

└── README.md

```



\## Data Model



The MySQL data warehouse uses a star schema to support analytical reporting.



\### Dimension Tables



| Table | Description | Row Count |

|---|---|---:|

| DimCurrency | Cryptocurrency metadata | 78 |

| DimDate | Calendar and date attributes | 2,082 |

| DimPlatform | Social media platforms | 2 |



\### Fact Table



| Table | Grain | Row Count |

|---|---|---:|

| FactSocialEngagement | One row per social media post | 6,902 |



The fact table contains social engagement metrics, including likes, retweets, comments, impressions, and engagement scores.



\### Aggregation Tables



\- CurrencySummary

\- DailySocialSummary

\- SocialEngagementSummary

\- FactSocialEngagementEnriched



\### SQL Reporting Views



\- vw\_ExecutiveDashboard

\- vw\_PlatformDaily

\- vw\_SocialAnalytics

\- vw\_TimeSeries



Data dictionary:

Docs/data-dictionary.xlsx



\## Power BI Reports



\### Top Performers Report



\- Cryptocurrency engagement rankings

\- Conditional formatting

\- Social engagement trend analysis

\- Platform performance comparison

\- Currency-level analysis



\### Executive Dashboard



\- Key performance indicators

\- Interactive date filters

\- Dynamic Top N analysis

\- Platform comparison

\- Rolling engagement averages

\- Currency drill-through

\- Executive storytelling using bookmarks



\## Key Insights



Based on the displayed Power BI report:



\- Social Engagement Activity: 6,902 social engagement records across 33 active cryptocurrencies.

\- Leading Token: Magic Internet Money (MIMUSD) recorded the highest total engagements, with 676.

\- Engagement Concentration: The top three tokens account for approximately 28.9% of total engagements.

\- Average Engagement Score: The overall displayed average engagement score was 26.03.



These findings support social media engagement monitoring and cryptocurrency performance analysis.



\## Achievements



\- Developed an end-to-end Python ETL pipeline.

\- Loaded 6,902 social engagement records into MySQL.

\- Designed a star schema with three dimension tables and one fact table.

\- Created four aggregation tables and four SQL reporting views.

\- Developed two interactive Power BI reports.

\- Implemented DAX measures, filters, drill-through, and bookmarks.

\- Confirmed zero orphaned currency records during foreign key validation.

\- Confirmed aggregation coverage for all 33 currencies with social engagement data.

\- Prepared technical documentation and a project demonstration presentation.



\## Data Quality and Limitations



The pipeline includes missing-value checks, duplicate detection, currency symbol standardisation, foreign key validation, and reject handling.



The currency foreign key validation identified no orphaned records. However, the Task 6 reject-validation logic and missing influence classifications require further investigation.



The pipeline currently runs through manual Jupyter notebook execution. Automated scheduling and scheduled Power BI refresh are potential future enhancements.



\## Documentation



\- Technical Runbook: Docs/technical-runbook.md

\- User Guide: Docs/user-guide.md

\- Architecture Diagram: Docs/architecture-diagram.png

\- Data Dictionary: Docs/data-dictionary.xlsx



\## Demo



Demo video URL: \[Add demo video link after recording]



Presentation:

Docs/demo-presentation.pptx



\## Contact



Sachini Morawinnage



Master of Information Technology



Email: smmorawinnage@gmail.com



GitHub: https://github.com/SachiniM96



Portfolio: https://sachinim96.github.io/sachini-portfolio/



