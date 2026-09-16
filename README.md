# MSBA 265 - Foundational Module 1

## Interactive EDA, Data Quality Verification, Data Dictionary & Outlier Pipeline

This project analyzes the French Motor Third Party Liability Claims dataset (`freMTPL2freq`).

## Dataset

- Source: OpenML
- OpenML ID: 41214
- Original records: 678,013
- Final cleaned records: 600,447

## Setup Instructions

Follow these steps to run the notebook on your own machine.

1. **Clone the repository**
   ```bash
   git clone https://github.com/luckynnmn/msba-265.git
   cd msba-265
   ```

2. **Create a virtual environment**
   ```bash
   python -m venv venv
   ```

3. **Activate the virtual environment**
   - Windows (PowerShell):
     ```powershell
     .\venv\Scripts\Activate.ps1
     ```
   - Windows (Command Prompt):
     ```cmd
     venv\Scripts\activate.bat
     ```
   - macOS / Linux:
     ```bash
     source venv/bin/activate
     ```

4. **Install the required libraries**
   ```bash
   pip install -r requirements.txt
   ```

5. **Select the correct kernel in VS Code**
   Open `notebooks/01_eda_and_data_dictionary.ipynb`, then click the kernel picker in the top-right corner of the notebook and select the Python interpreter from the `venv` you just created and activated (e.g. `venv (Python 3.x)`).

6. **Download the raw dataset.**

```cmd
python data\download_data.py
```

Expected output:

```text
data/raw_business_data.csv
678,013 rows x 12 columns
```

7. **Run the notebook**
   Use **Run All** to execute the full notebook from top to bottom.

> **Troubleshooting:** If you see `ModuleNotFoundError` for a package like `matplotlib` or `seaborn`, it almost always means the notebook kernel is not pointed at the `venv` from step 2-4. Re-check step 5, then restart the kernel and re-run.

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

[View / Download Module 1 Report](https://github.com/luckynnmn/msba-265/blob/master/Module1%20Report.pdf)