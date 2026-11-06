# NextPlay Football Academy: Cloud Data Warehouse and Analytics Plan

> **Academic project.** Completed for a graduate course in the M.S. in Information Technology (Data Management and Analytics) program. The client is fictional, and this is a design and recommendation plan, not a live implementation.

## Overview

NextPlay is an imaginary small (under 50 employees), privately owned, on-ground youth football training academy in Virginia. I designed a cloud analytics, data warehousing, network, and security plan that would let the academy turn registration, payment, engagement, and attendance data into business decisions.

## What I designed

- **Cloud platform:** Microsoft Azure (public cloud), with Power BI Pro as the reporting layer.
- **Four data sources:** player registration and profiles, payment gateway transactions (Stripe/Square), website and social media engagement, and attendance/performance data from coaches' mobile app.
- **Data warehouse:** Azure Synapse Analytics (serverless SQL pool) with a star schema built around a session fact table (`FactSession`), and Azure Data Lake Storage Gen2 (Hot tier) as the staging layer.
- **Pipelines:** Azure Data Factory for ETL and Synapse Pipelines for ELT.
- **Network and security:** VLAN segmentation with a UniFi Dream Router, WireGuard VPN for admin remote access, Microsoft Defender for Business, Microsoft Entra ID multi-factor authentication, TLS 1.2/1.3 in transit and AES-256 at rest, and role-based access control. Data was classified as Confidential because it includes information about minors.

## Risk analysis

I built a quantitative risk model in Excel covering 20 risks, calculating asset value, single loss expectancy (SLE), annual rate of occurrence (ARO), annual loss expectancy (ALE), countermeasure cost, and ROI for each.

- Recommended 18 controls costing about $17K in total, reducing estimated annual loss on those risks from about $52K to about $12K (roughly 76%).
- Rejected 2 controls because their ROI was negative (a fire suppression system at the leased facility, and a dedicated HR-records access-control platform).

All figures are estimates based on documented assumptions.

## Diagrams

<!-- Upload your own image files to the docs folder using these exact names, or delete any line you don't have. -->

![Star schema](docs/star-schema.png)

![Data flow diagram](docs/data-flow-diagram.png)

![Network before and after](docs/network-before-after.png)

## Skills demonstrated

Data warehouse design (star schema), ETL/ELT pipeline design, cloud architecture on Azure, BI reporting with Power BI, quantitative risk analysis (ALE, ROI), network and security planning, and technical documentation.

## Author

**Abdullah Younas**
M.S. in Information Technology (Data Management and Analytics), Washington University of Science and Technology
[LinkedIn](https://www.linkedin.com/in/abdullah-younas-44476b449/)
