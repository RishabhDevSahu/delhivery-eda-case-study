# 🚚 Delhivery - Feature Engineering & Trip Efficiency Analysis 📊

## 🎯 Overview  
This project focuses on **feature engineering, exploratory analysis, and statistical validation** using Delhivery’s nationwide logistics trip dataset.  
The goal is to transform raw operational data into **structured, meaningful, and model-ready insights** to improve route efficiency, dispatch planning, and SLA accuracy.

---

## 🧩 Problem Statement  
Delhivery processes large-scale logistics data capturing timestamps, distances, trip durations, and routing metadata. However, the raw data contains **hidden inefficiencies, routing deviations, idle times, and undocumented operational delays**, making it difficult to use directly for planning, forecasting, or decision-making.

To enhance logistics intelligence, it is essential to:

- Identify where **route inefficiencies and bottlenecks** occur  
- Compare **real execution vs OSRM-estimated routing patterns**
- Detect **SLA breach risks and delay-prone hubs**
- Engineer **predictive, meaningful features** for future ML models  
- Enable actionable insights for operational optimization  

This analysis uncovers inefficiencies, quantifies deviation patterns, and prepares the dataset for forecasting and logistics optimization initiatives.

---

## 🛠️ Tech Stack

| Technology | Purpose |
|-----------|---------|
| 🧾 Pandas | Data cleaning & transformation |
| 🧮 NumPy | Numerical computation & efficiency metrics |
| 📘 SciPy (stats module) | Statistical testing (t-test, correlation, normality check) |
| ⚙️ Scikit-learn | Feature scaling (StandardScaler, MinMaxScaler) |
| 📊 Matplotlib | Visual exploration of operational trends |
| 🎨 Seaborn | Advanced analytical plotting for pattern recognition |

---

## 🔍 Key Insights

### 1️⃣ Delay Hotspots  
- **Gurgaon, Bhiwandi, and Bangalore** consistently show the highest delays.  
- These hubs require **workflow streamlining and faster dispatch coordination**.

---

### 2️⃣ Slow Corridor Scheduling  
- High creation-to-start gaps observed in **Assam → Maharashtra** and **AP → West Bengal** routes.  
- Indicates **planning and resource allocation delays**.

---

### 3️⃣ Actual vs Planned Distance Gap  
- Median route efficiency ratio: **~0.63**  
- Real on-ground routes are often **shorter than OSRM suggestions**.

---

### 4️⃣ Time Efficiency Deviation  
- Actual trips take **nearly 2× longer** compared to OSRM estimates.  
- SLAs, ETAs, and routing assumptions require recalibration.

---

### 5️⃣ FTL Dominates Delay Contribution  
- **~95.8%** of deviation originates from Full-Truck-Load shipments.  
- Targeted optimization here will produce **maximum operational benefit**.

---

### 6️⃣ Scan Timestamp as Forecasting Signal  
- Strong correlation: **0.91** between scan duration and total trip time.  
- Can be leveraged for **real-time delay prediction**.

---

### 7️⃣ Speed Benchmarks Unrealistic  
- **~99.8%** of trips exceed OSRM predicted speed.  
- OSRM parameters do not reflect real-world logistics constraints.

---

### 8️⃣ High-Efficiency Lanes Identified  
- **Chandigarh and Daman & Diu** demonstrate strong routing efficiency.  
- These regions can act as **best-practice models**.

---

### 9️⃣ Hidden Idle Time Exists  
- Paired t-test shows **trip duration > sum of segment duration**, meaning waiting, scanning, or depot idle time isn't recorded.

---

### 🔟 OSRM Distance Overestimation  
- Average discrepancy: **~2561 km** between estimated vs aggregated segment distance.  
- Suggests flawed distance aggregation or duplicated routing logic.

---

## ✅ Recommendations

| Focus Area | Action |
|-----------|--------|
| 🏭 Hub Optimization | Improve SOPs at Gurgaon, Bhiwandi & Bangalore |
| 🚚 Dispatch Automation | Reduce planning delays on slow corridors |
| 🗺 Routing Calibration | Use real driving traces instead of only OSRM assumptions |
| ⏱ SLA Reset | Update ETA expectations to match real performance |
| 🚛 Prioritize FTL | Audit and optimize FTL scheduling and routing |
| ⚠ Predictive Alerts | Use scan duration anomalies for early warning |
| 📌 Continuous Calibration | Compare planned vs actual metrics monthly |
| 🚨 Outlier Rules | Flag trips taking >2× OSRM time |
| 🔍 Idle Time Logging | Capture handoff, waiting, and queue delays |
| 📈 Benchmark Best States | Apply best performing routing strategies nationwide |

---

## 🚀 Future Enhancements

- Trip delay prediction using ML  
- SLA breach early-warning analytics  
- Real-time anomaly flagging  
- Route optimization engine  
- Operations team dashboard for trip health monitoring  

---

## 📚 Conclusion  
This project demonstrates how **feature engineering + data analysis + statistical validation** can extract meaningful logistics intelligence from raw operational trip data.

The refined dataset supports:

- Accurate SLA and ETA forecasting  
- Better route planning and trip prioritization  
- Stronger anomaly detection  
- Scalable predictive analytics  

This contributes to Delhivery’s mission of **efficient, predictable, and data-driven logistics execution.**

---

## 📜 License  
This project is intended for educational and analytical learning purposes.

---

⭐ If you find this project useful, **consider giving it a star!**
