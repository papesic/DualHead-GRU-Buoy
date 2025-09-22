# Dual-Head GRU for Predicting Dangerous Sea Conditions and Wave Heights

This project explores forecasting **dangerous sea states** using buoy sensor data.  
A **dual-head GRU with attention pooling** was trained to:
1. Classify if a dangerous wave condition will occur within the next 6 hours.  
2. Forecast the mean significant wave height (WVHT) over the same horizon.  

Full methodology and results are in [`report/Dual-Head_GRU_Report.pdf`](report/Dual-Head_GRU_Report.pdf).

---

## Key Features
- Dataset: Irish Weather Buoy Network (2001–2017)  
- Preprocessing: gap-filling, cyclical time encoding, missingness indicators  
- Model: GRU + attention pooling with dual heads (classification + regression)  
- Techniques: Focal Loss, weighted sampling, temperature scaling, MC Dropout for uncertainty  
- Results:  
  - Classification AUC: **0.936–0.974**  
  - Regression R²: up to **0.933**  

---

## Repository Structure
notebooks/ # Jupyter notebooks for exploration, preprocessing, training
report/ # Final PDF report
README.md # This file
requirements.txt # Dependencies

## Notebooks
- `1_Data_exploration.ipynb` → Exploratory data analysis  
- `2_Data_preprocessing.ipynb` → Cleaning, feature engineering, dataset splits  
- `3_GRU_model.ipynb` → Model training, evaluation, and results  

---

## Dataset

- Raw buoy data can be downloaded from [Kaggle](https://www.kaggle.com/datasets/mahdiehhajian/weather-buoy-network) or [Marine Institute](https://data.gov.ie/publisher/marine-institute).  
---

