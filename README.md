# Distribution Shift Audit & Impact Quantification

## Project Overview
This repository contains a rigorous statistical audit of covariate distribution shift, evaluating how a "Black Swan" macroeconomic event degrades predictive logistics models. 

Using the U.S. Flight Delay dataset, the data was partitioned into two distinct temporal windows:
* **Training Window (Baseline):** 2019 (Stable, pre-pandemic operational volume)
* **Serving Window (Shock):** 2020 (Pandemic onset, characterized by systemic anomalies)

The objective is to detect, characterize, and quantify the distribution shift between these windows, compute covariate shift via density ratio estimation, and measure the downstream R² degradation of a baseline regression model.

## Repository Contents
1. `flight_delay_audit.ipynb`: The sequential, fully commented Python notebook containing data loading, Population Stability Index (PSI) auditing, density ratio estimation, and model performance evaluation.
2. `Distribution_Shift_Report.pdf`: A 2-page executive summary detailing the nature of the shift, root cause analysis, and feature-level remediation priorities for the ML Engineering team.
3. `requirements.txt`: Python package dependencies.

## Setup Instructions

**1. Clone the repository:**
```bash
git clone [https://github.com/Priyanka638191/Novintix-Distribution-Shift-Audit.git]
cd Novintix-Distribution-Shift-Audit

2. Install dependencies:

Bash
pip install -r requirements.txt
3. Download the Dataset:
Due to file size limits, the raw dataset is not hosted in this repository.

Download the Airline_Delay_Cause.csv from Kaggle's Flight Delay Data.

Place the Airline_Delay_Cause.csv file directly in the root directory of this repository.

4. Run the Audit:

Launch Jupyter Notebook:

Bash
jupyter notebook
Open flight_delay_audit.ipynb and select "Restart & Run All" to sequentially execute the pipeline and reproduce the degradation metrics.
