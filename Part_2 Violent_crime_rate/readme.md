
### 🧱 Database Structure

The dataset is organized into four relational tables:

1. **states** – Contains U.S. state details.  
   - `state_id` (PK), `state_code` (INT), `state_full_name`

2. **counties** – Lists counties and links them to states.  
   - `county_id` (PK), `county_name`, `county_code` (INT), `state_id` (FK)

3. **measures** – Defines health-related metrics.  
   - `measure_id` (PK), `measure_name`

4. **health_statistics** – Fact table with health data per county and measure.  
   - `stat_id` (PK), `state_id` (FK), `county_id` (FK), `year_span`, `measure_id` (FK), `numerator`, `denominator`, `raw_value`, `confidence_interval_lower`, `confidence_interval_upper`, `data_release_year`, `fipscode`
🔍 Problem Statement & Objective
This project focuses on analyzing County Health Rankings with an emphasis on violent crime rates across U.S. states and counties.

Problems to Address:
Calculate the average violent crime rate by state, and break it down by county to analyze local variations, excluding national-level data and non-state districts (e.g., Washington, D.C.).

Identify the counties with the highest violent crime rates within each state.

➡️ Current Focus: I am currently working on solving the above problems using SQL-based queries and data modeling.
