# 🧠 US County Health Rankings Analysis

This is a multi-part project focused on analyzing U.S. County Health Rankings using a relational database and SQL. The goal is to break down complex public health data, design a normalized schema, and derive insights through SQL queries.

---

## 📁 Project Structure

The initial dataset was normalized into **4 relational tables** to support scalable and efficient querying:

1. **`states`** – Contains state-level information (`state_id`, `state_code`, `state_full_name`)
2. **`counties`** – County data linked to states (`county_id`, `county_name`, `state_id`)
3. **`measures`** – Definitions of health metrics (`measure_id`, `measure_name`, `category`)
4. **`health_statistics`** – Fact table with raw values by county, year, and metric (`stat_id`, `county_id`, `measure_id`, `raw_value`, `year`)

Each part of the project will address different public health questions using this schema.

---

## 🛠️ Tools Used

- **PostgreSQL** – Core database engine
- **SQL** – For querying, analysis, and transformations
- **pgAdmin** (optional) – GUI for managing PostgreSQL databases
- **Spreadsheet Software** – Used during initial data exploration and schema planning

---

## 📦 Parts

- [`part_1(Crime rate Analysis)`](part_1/) – RDBMS setup and violent crime rate analysis

Stay tuned for additional parts covering other metrics and visualizations.


