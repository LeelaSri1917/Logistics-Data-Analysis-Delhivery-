# Logistics-Data-Analysis-Delhivery-
This project presents an in-depth analysis of logistics data from Delhivery, a leading supply chain services company. Using Python and data science techniques, the notebook explores shipment patterns, delivery timelines, and performance indicators.


**Type:** Data Analytics / Exploratory Data Analysis (EDA)  
**Tools Used:** Python, Pandas, NumPy, Matplotlib, Seaborn, Scikit-learn, SciPy

---

## 📌 **Objective**

To perform **exploratory data analysis (EDA)**, **feature engineering**, and **statistical testing** on delivery trip data to understand patterns in **time**, **distance**, **delivery performance**, and **operational behavior**.

---

## 📂 **Dataset Overview**

The dataset includes **24 columns** with **trip-level segment data** for deliveries:

- ⏱ **Timestamps:** `trip_creation_time`, `od_start_time`, `od_end_time`
- 📍 **Source/Destination Info:** `source_center`, `destination_center`, `source_name`, `destination_name`
- 📏 **Time & Distance Metrics:** `actual_time`, `osrm_time`, `actual_distance_to_destination`, etc.
- 🔄 **Segment-Level & Total Route Data**

---

## 🔧 **Steps Performed**

### 1. 📥 **Data Preprocessing**
- Converted datatypes (`datetime64`, `category`)
- Replaced nulls in `source_name`, `destination_name` with `"UNKNOWN"`
- Removed columns: `cutoff_factor`, `segment_factor`
- Dropped duplicates and cleaned data anomalies

### 2. 📊 **Exploratory Data Analysis**
- Analyzed trip frequencies by **day, week, and month**
- Identified **top source and destination** states & cities

### 3. 🧮 **Feature Engineering**
- Extracted:
  - `trip_creation_hour`
  - `weekday`, `month`, `weekofyear`
- Parsed location fields into **city** and **state**

### 4. 🧪 **Hypothesis Testing**
- **Shapiro-Wilk Test** for normality
- **Mann-Whitney U Test** comparisons:
  - `actual_time` vs `osrm_time`
  - `od_total_time` vs `start_scan_to_end_scan`
  - Segment-level vs trip-level metrics

### 5. 🧼 **Outlier Detection**
- Applied **IQR method** to detect outliers in:
  - Time-related fields
  - Distance-related fields

### 6. ⚖️ **Feature Scaling**
- Scaled numerical columns using:
  - `MinMaxScaler`
  - `StandardScaler`  
  (for future ML modeling)

---

## 📈 **Key Insights**

- 🕒 **87.9% of trips** were created in **September**
- 📆 **Peak trip creation time**: **10 P.M**
- 🚛 **Carting trips**: **60.2%**, **FTL**: **39.8%**
- 🌆 **Top Cities**: Mumbai, Bengaluru, Gurgaon dominate source/destination
- 🧪 **Statistical tests** reveal **significant difference** between predicted (OSRM) and actual time/distance — **OSRM engine requires optimization**

---

## ✅ **Final Recommendations**

- 🔧 **Improve OSRM Routing Engine** for better ETA/distance prediction
- 🏙 **Analyze congested cities/states** for traffic-driven delays
- 🚚 Optimize **FTL route planning** for long-distance efficiency
- 🧽 Clean and enrich **missing location fields**
- ⌚ Use **peak delivery time insights** for resource scheduling
- 🚨 Investigate and reduce **extreme outliers** in time & distance

---

## 📬 **Contact**

**Leela Sri Mekala**  
📧 [YourEmail@example.com]  
🔗 [LinkedIn Profile](https://linkedin.com/in/your-profile)

---

## 📁 **Run This Project**

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/delhivery-trip-analysis.git
