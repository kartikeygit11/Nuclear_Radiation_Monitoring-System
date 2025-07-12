# Nuclear Radiation Monitoring System 🛡️

![Cooling‑tower of a nuclear power plant](https://cdn.pixabay.com/photo/2019/07/19/23/16/power-plant-4349830_640.jpg)

A lightweight **Streamlit** application that shows your proximity to nuclear power‑plant reactors, flags potential radiation‑risk zones, and notifies you in real time. Upload a CSV of plant locations, let the app detect your location, and instantly visualise safe, moderate, and dangerous zones on an interactive map.

---

## ✨ Features

- **CSV Upload** – Ingest any plant dataset (`Name, Latitude, Longitude, Age`) on the fly.  
- **Auto Geolocation** – Gets your current lat/long via IP (fallback = 0, 0).  
- **Dynamic Safety Scoring** – Classifies reactors as **Safe**, **Moderate**, or **Dangerous** based on simple age thresholds (customisable).  
- **Interactive Map** – Renders colour‑coded radius circles with [`folium`](https://python-visualization.github.io/folium/) right inside Streamlit.  
- **Distance Check** – Warns if a reactor ≤ 500 km of you crosses a risk threshold.  
- **Desktop Alerts** – Pops native OS notifications via `plyer` so you don’t miss a critical warning.  

---

## 🏗️ Tech Stack

| Layer        | Library / Tool |
|--------------|----------------|
| UI           | Streamlit |
| Mapping      | Folium + streamlit‑folium |
| Geolocation  | geocoder, geopy |
| Notifications| plyer |
| Data         | pandas, CSV |

---

## 🚀 Quick Start

```bash
# 1. Clone the repo
git clone https://github.com/kartikeygit11/Nuclear_Radiation_Monitoring-System.git
cd Nuclear_Radiation_Monitoring-System

# 2. Create & activate a virtual environment (optional but recommended)
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate

# 3. Install dependencies
pip install -r requirements.txt
pip install streamlit folium streamlit_folium geocoder plyer

# 4. Launch the app
streamlit run main.py
