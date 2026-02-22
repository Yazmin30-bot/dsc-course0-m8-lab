# Aviation Accident Analysis

# Aviation Accidents Analysis: Insurance Risk & Safety Recommendations

## Project Overview
This project was developed for an aviation insurance consulting firm to identify high-safety/low-risk aircraft for commercial and private use. The analysis evaluates aircraft makes and models based on two primary safety metrics: 
1. **Total Destruction Rates** (Structural Integrity)
2. **Serious/Fatal Injury Likelihood** (Passenger Survivability)

The study focuses exclusively on professional builds manufactured or operational from **1983 to 2023** to ensure all recommendations are relevant to active modern fleets.

## Repository Structure
* **`Aviation_Accidents_Cleaning.ipynb`**: Contains the data pipeline for cleaning raw NTSB records. This includes handling missing values, filtering for "Professional" builds, and restricting the timeframe to the last 40 years.
* **`Aviation_Accidents_Data_Analysis.ipynb`**: The exploratory data analysis (EDA) phase. This notebook contains the statistical logic, visualizations, and comparative grouping used to derive the final safety recommendations.
* **`cleaned_aviation_data.csv`**: The refined dataset containing engineered features such as `Serious_Fatal_Rate`, `is_destroyed`, and `Plane Type` (a combination of Make and Model).

## Data Processing & Feature Engineering
To provide statistically robust insights, the following transformations were applied:
* **Temporal Filtering**: Data limited to 1983–2023 to reflect current aviation standards.
* **Serious_Fatal_Rate**: Calculated as the ratio of (Fatal + Serious Injuries) to the total number of passengers.
* **is_destroyed**: A boolean flag derived from the `Aircraft.damage` column to track hull losses.
* **Sample Size Validation**: Analysis was restricted to makes/models with enough data points to ensure statistical significance.

## Key Insights & Findings

### 1. Manufacturer Performance
* **For Durability (Hull Integrity):** Choose **Diamond** (Small) or **Aerospatiale/Boeing** (Large). These manufacturers show the lowest rates of aircraft being classified as "Destroyed."
* **For Survivability (Passenger Safety):** Choose **Waco** (Small) or **Airbus/Boeing** (Large). These brands consistently show higher rates of uninjured or minor-injury outcomes in the event of an accident.

### 2. Insurance Risk Profiling
* **Optimal Investment:** **Boeing and Airbus** remain the most statistically robust choices for large-scale investment. Their aircraft exhibit a consistent "zero-injury" clustering across massive datasets, indicating high reliability.
* **Structural Safety:** For the lowest overall insurance risk, Boeing and Airbus are preferred for large fleets, while **Diamond** is the standout modern choice for small-aircraft structural safety.

### 3. Fleet Recommendations
* **For Large Fleets:** The **Boeing 737** (various series) and **McDonnell Douglas MD-80/90** series are highly recommended for insurers due to their low injury volatility and proven track records.
* **For Small Operations:** The **Diamond DA 20** is the premier choice for modern safety. For utility or rugged operations, the **Maule M-4** and **Cessna 180** series are preferred due to their high survivability records in varied terrain.

### 4. Environmental & Technical Factors
* **Weather Impact:** Visibility is a critical risk multiplier. Accidents in **Instrument Meteorological Conditions (IMC)** are 2–3× more likely to result in fatal injuries compared to **Visual Meteorological Conditions (VMC)**.
* **Engine Type:** **Turbofans (Jets)** are the safest category. **Reciprocating (Piston)** engines carry the highest insurance risk, as single-engine failures in this category provide the lowest margin for error.

## Requirements
* Python 3.x
* Pandas
* NumPy
* Matplotlib
* Seaborn

[DSC Course M8 Lab Repository](https://github.com/Yazmin30-bot/dsc-course0-m8-lab)


