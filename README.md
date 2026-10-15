Kenya Malaria Surveillance Analysis

Project Overview

This project explores monthly malaria incidence across 47 Kenyan counties from 2015 to 2025 using Python. It combines exploratory data analysis with a preliminary one-month-ahead prediction experiment to investigate how a simple machine-learning model compares with a seasonal baseline.

The project was developed as a learning portfolio project focused on public-health analytics and disease surveillance.

Objectives

- Explore temporal patterns in malaria incidence.
- Assess dataset completeness and monthly continuity.
- Develop a preliminary one-month-ahead prediction model.
- Compare linear regression against a seasonal baseline.
- Reflect on the limitations of predictive modelling for public-health surveillance.

Tools and Technologies

- Python
- Pandas and NumPy
- Matplotlib
- Scikit-learn
- Google Colab

Dataset

The supplied dataset contains 6,110 county-month records and 22 columns, covering March 2015 to December 2025. The columns include malaria incidence, environmental variables, intervention coverage, population density, and lagged variables.

The dataset was obtained from a "Zenodo record" (https://zenodo.org/records/20051237). Its provenance, methodology, and licensing require verification; therefore, the analysis should not be interpreted as an independently verified representation of official Kenyan malaria surveillance data.

Data Quality Checks

Initial checks found:

- 6,110 rows and 22 columns.
- 47 counties represented.
- No missing values in the supplied columns.
- No duplicate county-month records.
- Continuous monthly records for each county over the dataset period.

These checks assess structural completeness and consistency; they do not establish the accuracy of the underlying measurements.

Prediction Experiment

The target was malaria incidence in the following month. I compared two approaches:

1. Seasonal baseline: Uses incidence from the same calendar month in the previous year.
2. Linear regression: Uses current-month incidence and selected environmental and county-level variables to estimate next-month incidence.

The data were split chronologically, with training target dates before January 2023 and test target dates from January 2023 through December 2025.

Results

Test period| Linear regression MAE| Seasonal baseline MAE
2023| 2.553| 3.627
2024| 2.568| 3.162
2025| 2.424| 3.056
Overall| 2.515| 3.282

The linear regression model reduced overall mean absolute error (MAE) by approximately 23.4% compared with the seasonal baseline on the test set. It also achieved a lower MAE than the baseline in each test year.

MAE measures the average absolute difference between predicted and observed incidence, expressed in the target's units (incidence per 1,000).

Limitations and Next Steps

This is an exploratory learning project, not a validated operational forecasting system.

- Dataset provenance, measurement methods, and licensing need further verification.
- Predictor availability at the time a real forecast would be issued needs to be assessed.
- A small number of linear regression predictions were negative, which is not meaningful for malaria incidence.
- Further work could explore non-negative prediction methods, additional validation strategies, and comparisons with other forecasting approaches.

Learning Outcomes

This project strengthened my practical understanding of data cleaning, exploratory analysis, chronological train-test splitting, regression modelling, baseline comparisons, and evaluation using MAE. It also highlighted the importance of data provenance, realistic prediction settings, and communicating model limitations in public-health applications.

Reproducibility

The analysis notebook and its code are available in this repository. The original dataset is not redistributed here because its licensing and redistribution permissions have not yet been verified.
