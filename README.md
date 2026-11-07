<div align="center">

# 🌾 FasalAlert — Crop Stress & Weather Risk Advisory

**Which Indian districts' crops are under weather stress right now, and what should farmers do?**
Live weather compared against IMD climate normals and the ICAR crop calendar, scored per crop and growth stage, mapped across India.

[![Upstream](https://img.shields.io/badge/Team_repo-SpatioFarm-00d4ff?style=for-the-badge&logo=github&logoColor=white)](https://github.com/SpatioFarm/fasalalert)
[![Report](https://img.shields.io/badge/Project_report-Read-00ff88?style=for-the-badge&logo=microsoftword&logoColor=white)](docs/FasalAlert_Report.docx)

![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white)
![GeoPandas](https://img.shields.io/badge/GeoPandas-139C5A?logo=pandas&logoColor=white)
![Folium](https://img.shields.io/badge/Folium-77B829?logo=leaflet&logoColor=white)
![OpenWeatherMap](https://img.shields.io/badge/OpenWeatherMap_API-EB6E4B)

</div>

---

## 🔍 What it does

- **Live weather, any district** — fetches current conditions from OpenWeatherMap for Indian districts.
- **Anomaly, not raw weather** — compares temperature, rainfall and humidity against IMD district climate normals.
- **Crop- and stage-aware score** — the Crop Stress Score (CSS) uses per-crop, per-stage thresholds and weights, and separates heat from cold, excess rain from deficit, high humidity from low.
- **Pan-India map** — an interactive district choropleth shows where stress is building.
- **Advisories** — stressed districts get actionable guidance.

## 🛰️ Data

**IMD** district climate normals · **ICAR** crop calendar · **GADM** district boundaries · **OpenWeatherMap** live weather

## 🚀 Run it yourself

```bash
git clone https://github.com/SpatioFarm/fasalalert.git
cd fasalalert
pip install -r requirements.txt
python main.py
```

<details>
<summary><b>Folder layout</b></summary>

```
data/                     GeoJSON boundaries, IMD normals, crop calendar and thresholds
docs/                     project report
src/gui/app.py            Streamlit dashboard
src/logic/stress.py       CSS formula and classification
src/logic/spatial.py      GeoPandas and Folium map
src/utils/weather_api.py  OpenWeatherMap calls
src/utils/helpers.py      anomaly calculator and advisory
main.py                   entry point
```

</details>

## 👥 Team

SpatioFarm · Python project, M.Sc. Agriculture Analytics (DAU · AAU · IIRS-ISRO), 2026

| Member | Built |
|---|---|
| **Sathwik Ramaka** | `app.py` — Streamlit dashboard · [GitHub](https://github.com/sathwikramaka) |
| **Swathi A Patil** | `stress.py`, `crop_thresholds.json`, `crop_calendar.json` |
| **Kadiri Yaswanthi** | `weather_api.py` — OpenWeatherMap API |
| **Himanshu Bhanja** | `spatial.py`, `helpers.py`, repo setup |

<sub>This is a fork of the team repository [SpatioFarm/fasalalert](https://github.com/SpatioFarm/fasalalert).</sub>
