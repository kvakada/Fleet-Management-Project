# Fleet Insight Dashboard

A modern, data-driven dashboard designed to help fleet managers monitor vehicle performance, identify underutilized assets, and optimize operational decisions using real-time insights.

## 🚗 Project Overview

**Fleet Insight Dashboard** is a web application developed using **Dash (Plotly)**, designed to analyze and visualize key metrics from fleet vehicles, including:

* Downtimes (accidents, traffic, maintenance)
* Maintenance needs and predictions
* Accident probability insights
* Vehicle positioning on an interactive map
* Driver and vehicle overview analytics

## 📊 Key Features

* **Home (Map View):** Real-time interactive Mapbox view of all vehicles with filters for individual license plates.
* **Downtimes Dashboard:** View and filter vehicles experiencing issues like accidents, maintenance, or being idle.
* **Vehicle Overview:** Analyze vehicle distribution by class, vocation, type, and explore driver-level details.

## 🧠 Data Sources

This project uses simulated and preprocessed CSV datasets stored locally:

* `vehicle_data.csv`: Contains metadata and status of fleet vehicles.
* `fleet_data.csv`: Driving history including distances and IDs.
* `names.csv`: (Optional) Driver information (e.g., first/last name, email).

> These CSVs can be replaced with database connections if needed (`database_connection.py` supports PostgreSQL).

## 🛠️ Tech Stack

* **Frontend / Dashboard:** Dash, Plotly, Dash Bootstrap Components
* **Backend / Data Handling:** Python (Pandas, NumPy, Statistics)
* **Visualization:** Plotly Graphs, Mapbox for geospatial data
* **Deployment Ready:** Can be deployed using [Render](https://render.com/), Docker, or Gunicorn (for GCP)

## 📁 Folder Structure

```
apps/
├── downtimes.py         # Downtime dashboard view
├── home.py              # Map and high-level KPIs
├── vehicles_overview.py # Vehicle/driver breakdown
assets/
├── style.css            # Custom styles
main.py                  # App entrypoint
requirements.txt         # Dependencies for deployment
database_connection.py   # Optional DB connection setup
vehicle_data.csv         # Vehicle dataset
fleet_data.csv           # Driving behavior dataset
names.csv                # Driver info dataset (optional)
```

## 🚀 Getting Started

1. **Install dependencies**

   ```bash
   pip install -r requirements.txt
   ```

2. **Run the app**

   ```bash
   python3 main.py
   ```

   > If using Dash v2.0+, make sure `app.run()` is used instead of `app.run_server()`

3. **View in browser**

   * Navigate to `http://127.0.0.1:8050`

## 🌐 Deployment

You can deploy this dashboard using:

* [Render.com](https://render.com/docs/deploy-dash)
* Docker
* Heroku (if using a Gunicorn server)
* Google Cloud App Engine (using `app.yaml` and a PostgreSQL DB)

## 🧪 Future Enhancements

* Add login/authentication (e.g., Flask-Login)
* Integrate real-time streaming data (e.g., MQTT or WebSockets)
* Migrate from CSV to a PostgreSQL backend
* Incorporate advanced ML-based maintenance prediction

## 👨‍💻 Author

Built by [Karthik Vakada](https://github.com/kvakada) for portfolio and academic demonstration purposes.


