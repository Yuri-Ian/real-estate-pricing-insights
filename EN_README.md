## 📖 Project Description
- Exploratory analysis of **Yandex Real Estate** data (MAU ~39M users) to uncover the factors influencing apartment prices and time-on-market in **St. Petersburg, Russia, and its surrounding suburbs**.  
- Saint Petersburg — Russia’s second-largest city — has an estimated population of **5.6M (2024)** and spans approximately **1,400 km²**.  
The broader metropolitan area, including nearby suburbs, covers about **12,600 km²** with a population of roughly **6.4M**.  
- This context highlights the scale of the housing market analyzed in this project. The study provides pricing benchmarks by **location** and **distance to the city center**, supporting data-driven decisions on pricing, buying, and selling.

---

## 🎯 Project Goal
To build a **reproducible analytical pipeline** that:  
- Cleans and preprocesses raw data.  
- Engineers new features.  
- Analyzes distributions and dependencies.  
- Identifies key factors affecting price and time-to-sell.  
- Builds benchmarks by locality and distance to center.  
- Summarizes insights with recommendations.  

---

## 🛠️ Tasks
- Conduct a basic data audit.  
- Detect and process missing values.  
- Normalize column types, fix duplicates and anomalies.  
- Clean up dictionaries (e.g. `locality_name`).  
- Add new features:  
  - price per sqm,  
  - posting weekday/month/year,  
  - floor category (“first”, “last”, “other”),  
  - distance to city center (km).  
- Analyze key parameters: size, price, rooms, ceiling height, floor type, distance to center, parks.  
- Study **time-on-market (`days_exposition`)** distribution (histogram, mean/median, thresholds for “fast” vs. “long” sales).  
- Calculate avg price per sqm in top-10 localities; highlight most expensive and cheapest ones.  
- For St. Petersburg: evaluate average price by distance (km) from center; build visualization and interpret trend.  
- Provide interim and final conclusions.  

---

## 📊 Dataset
We use **archival listings data from Yandex Real Estate** covering apartments in St. Petersburg and nearby localities over several years.  
- **User-provided fields:** price, area, rooms, ceiling height, etc.  
- **Auto-generated fields (geo-based):** distance to center, distance to airport, number of parks/water bodies nearby.  

---

## 🔑 Major Insights
- **Data preprocessing** removed noise (rare/extreme values) and filled logical defaults (e.g. 0 balconies, median ceiling height).  
- **Key price drivers:**  
  - total area (strong positive correlation),  
  - living area,  
  - kitchen area,  
  - floor type (first/last cheaper),  
  - posting year (captures market cycles).  
- **By locality:**  
  - St. Petersburg leads in avg sqm price, followed by Repino, Zelenogorsk, Pushkin (prestige, infrastructure, proximity).  
  - Lowest sqm prices: Sovkhozny, Efimovsky, Malaya Romanovka, others with weak demand/infrastructure.  
- **By distance:**  
  - Prices peak within 3 km of city center,  
  - Drop sharply after 5 km,  
  - Stabilize after 10 km,  
  - Show anomalies after 20–25 km (prestige suburbs).  

---

## ✅ Conclusion
Apartment pricing in St. Petersburg is shaped primarily by **size, location, and floor type**.  
**Central districts and prestigious suburbs** retain the highest values, while **remote localities** offer significantly cheaper housing due to weaker infrastructure and demand.  

---

## 📂 Repository Structure
- `project.ipynb` — full analysis notebook.  
- `EN_README.md` — project description and results in English.
- `RU_README.md` — project description and results in Russian.

---

## 📌 Notes
This is one of my **early projects**. At the time, my focus was on detailed manual EDA and careful documentation.  
Today, I would implement the same pipeline more efficiently — using automation, pipelines, and richer visual analytics.  
Keeping this notebook in its original form reflects my growth trajectory as a Data Analyst.  
