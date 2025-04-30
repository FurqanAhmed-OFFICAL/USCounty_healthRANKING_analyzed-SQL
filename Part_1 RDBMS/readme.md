# 🧩 Part 1: Relational Database Design (RDBMS)

This part of the project focuses on designing and implementing a relational database (RDBMS) to support the analysis of U.S. County Health Rankings. The raw dataset was initially flat and mixed, so it was restructured into normalized tables to improve clarity, reduce redundancy, and support advanced SQL querying.

---

## 🧱 Database Structure

The dataset was broken down into the following 4 relational tables:

### 1. `states`
- Contains information about U.S. states.
- Fields:
  - `state_id` – Primary key
  - `state_code` – INT 
  - `state_full_name` – Full name of the state (e.g., California)

### 2. `counties`
- Stores details about counties and links each one to a state.
- Fields:
  - `county_id` – Primary key
  - `county_name` – Name of the county
  - `county_code` – INT
  - `state_id` – Foreign key referencing the `states` table

### 3. `measures`
- Defines each health-related measure or indicator.
- Fields:
  - `measure_id` – Primary key
  - `measure_name` – Name of the metric (e.g., "Violent crime rate")


### 4. `health_statistics`
- Fact table that stores actual health values and metadata for each county and measure.
- Fields:
  - `stat_id` – Primary key
  - `state_id` – Foreign key to `states`
  - `county_id` – Foreign key to `counties`
  - `year_span` – Time span of the data (e.g., 2015–2017)
  - `measure_id` – Foreign key to `measures`
  - `numerator` – Raw count used in calculating the measure
  - `denominator` – Base count (e.g., population)
  - `raw_value` – Final calculated value
  - `confidence_interval_lower` – Lower bound of confidence interval
  - `confidence_interval_upper` – Upper bound of confidence interval
  - `data_release_year` – Year the data was published
  - `fipscode` – Federal Information Processing Standard code (geographic identifier)

> These tables follow proper normalization and establish clear relationships using primary and foreign keys.

---

## 🛠️ Tools Used

- **PostgreSQL**  
  Used to create the database, define tables, manage constraints, and store data.

- **SQL**  
  Used to write `CREATE TABLE` statements, enforce relationships, and prepare the schema.

- **Excel / Google Sheets**  
  Used for preliminary data exploration and identifying logical groupings for normalization.

---

## 🎯 Outcome

At the end of Part 1, the raw dataset is fully transformed into a structured and relational format using PostgreSQL. This schema forms the backbone for future parts of the project, where SQL queries will be written to extract insights, perform analysis, and solve real-world health-related questions.

