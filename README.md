# 🌦️ Weather ETL Pipeline

## 🧠 Overview

This project is an **ETL (Extract, Transform, Load)** data pipeline for weather data, built using:

- **Apache Airflow** for orchestration
- **Astro (Astronomer)** for streamlined pipeline deployment and DAG management
- **PostgreSQL** as the data warehouse for storage

It fetches weather data from an API, processes it, and stores the clean and structured data in a PostgreSQL database for downstream analytics.

---


---

## 🔄 ETL Workflow

1. **Extract**  
   - Pulls live weather data from a weather API (e.g. OpenWeatherMap)

2. **Transform**  
   - Cleans and normalizes temperature, humidity, pressure, wind, etc.
   - Converts timestamps and units

3. **Load**  
   - Inserts the processed data into a PostgreSQL database
   - Table is created using a pre-defined schema if not present

---

## 🛠️ Technologies Used

| Tool            | Purpose                           |
|-----------------|------------------------------------|
| Apache Airflow  | Workflow orchestration             |
| Astro CLI       | Run and manage Airflow projects    |
| PostgreSQL      | Data warehousing                   |
| Docker          | Containerized environment          |
| Python          | Data processing and API integration|

---
## 🧩 Database Schema
This project uses a PostgreSQL database to store weather data fetched via the ETL pipeline. The data is stored in a table named weather_data with the following schema:

| Column Name     | Data Type | Description                                        |
| --------------- | --------- | -------------------------------------------------- |
| `latitude`      | FLOAT     | Geographical latitude of the location              |
| `longitude`     | FLOAT     | Geographical longitude of the location             |
| `temperature`   | FLOAT     | Measured temperature in Celsius                    |
| `windspeed`     | FLOAT     | Wind speed (in km/h or m/s)                        |
| `winddirection` | FLOAT     | Direction of the wind (in degrees)                 |
| `weathercode`   | INT       | Encoded weather condition (e.g., 0 = clear)        |
| `timestamp`     | TIMESTAMP | Time of data collection (defaults to current time) |



## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/weather-etl-pipeline.git
cd weather-etl-pipeline




