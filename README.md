# Healthcare Research Data Analysis

This repository contains a Jupyter Notebook designed for processing, analyzing, and deriving insights from healthcare and fitness-related data collected from various sources, including Fitbit, Google Docs, and PMSys. The data includes heart rate, sleep, activity levels, and subjective wellness reports from multiple participants.

## Table of Contents
- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Data Processing](#data-processing)
- [Analysis & Insights](#analysis--insights)
- [References](#references)

## Project Overview
This project processes and analyzes time-series data related to health and fitness, specifically looking at:
- Physical activity levels
- Heart rate and Heart Rate Variability (HRV)
- Sleep patterns and quality
- Stress and wellness factors
- Exercise tracking

The Jupyter Notebook extracts, cleans, processes, and visualizes this data to understand correlations between different health factors.

## Data Sources
The dataset is structured into multiple folders:
1. **Fitbit Data**
   - `exercise.json`: Detailed workout data
   - `calories.json`: Calories burned per minute
   - `steps.json`: Step count per minute
   - `distance.json`: Distance moved per minute
   - `sedentary_minutes.json`: Total sedentary time per day
   - `lightly_active_minutes.json`: Light activity minutes per day
   - `moderately_active_minutes.json`: Moderate activity minutes per day
   - `very_active_minutes.json`: High activity minutes per day
   - `heart_rate.json`: Heart rate readings per minute
   - `resting_heart_rate.json`: Daily resting heart rate
   - `time_in_heart_rate_zones.json`: Time spent in different heart rate zones
   - `sleep_score.csv`: Sleep analysis including quality and duration
   - `sleep.json`: Sleep breakdown into light, deep, and REM phases

2. **Google Docs Data**
   - `reporting.csv`: Self-reported meals, hydration, weight, and alcohol consumption

3. **PMSys Data**
   - `injury.csv`: Injury records with severity levels
   - `srpe.csv`: Perceived exertion scores from training sessions
   - `wellness.csv`: Self-reported wellness scores (fatigue, mood, sleep quality, soreness, stress, readiness)

## Data Processing
### Loading and Structuring Data
- The script reads and merges data from JSON and CSV files across multiple participants.
- It processes time-series data by normalizing timestamps and calculating relevant features.

### Data Cleaning & Transformation
- Missing values are handled appropriately.
- Heart Rate Variability (HRV) is computed from heart rate data.
- Activity durations are standardized across time.

### Feature Engineering
- HRV statistics are computed at different time resolutions.
- Training load and stress levels are inferred from multiple sources.
- Aggregations and pivots are performed for participant-level analysis.

## Analysis & Insights
### Correlation Analysis
- Examines relationships between stress, HRV, activity levels, and sleep quality.

### Statistical Testing
- Uses **t-tests** to compare HRV variations in different activity states (active vs. anxious states).

### Data Visualization
- **Scatter plots** to visualize relationships between stress and HRV.
- **Bar plots** to show correlation differences among participants.
- **Histograms** to analyze HRV distributions in different states.

## References
- [NCBI Research on Stress and HRV](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC8749560/)
- [HRV Analysis Guide](https://compscipal.medium.com/exploring-heart-rate-variability-hrv-d7a3d66bc4f2)
- [Firstbeat Stress & HRV Whitepaper](https://assets.firstbeat.com/firstbeat/uploads/2015/10/How-to-Analyze-Stress-from-Heart-Rate-Variability.pdf)
