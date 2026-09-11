# MSBA 265 - Foundational Module 1

## Interactive EDA, Data Quality Verification, Data Dictionary & Outlier Pipeline

This project analyzes the French Motor Third Party Liability Claims dataset (`freMTPL2freq`).

## Dataset

- Source: OpenML
- OpenML ID: 41214
- Original records: 678,013
- Final cleaned records: 600,447

## Project Contents

- `data/raw_business_data.csv` - Raw business dataset
- `data/cleaned_business_data.csv` - Cleaned dataset after outlier filtering
- `data/download_data.py` - Script used to download the dataset
- `notebooks/01_eda_and_data_dictionary.ipynb` - EDA and data dictionary analysis
- `src/clean_outliers.py` - Production outlier-cleaning pipeline
- `reports/data_dictionary.csv` - Business data dictionary
- `reports/figures/` - Analysis figures and visualizations

## Analysis

The project includes:

- Data structure and quality checks
- Raw boundary verification
- Business data dictionary
- Skewness analysis
- Pearson correlation analysis
- Distribution analysis
- Outlier detection using Tukey's 1.5 × IQR method

## Final Homework Report
[View / Download Module 1 Report](./Module1%20Report.pdf)