# kenya-malaria-surveillance-analysis.
Exploratory analysis of monthly county-level malaria incidence data using Python and Pandas.
Exploratory Analysis of Malaria Surveillance Data

Project overview

This beginner-level public-health data project uses Python and Pandas to examine temporal patterns in a supplied county-level malaria incidence dataset covering March 2015 to December 2025.

The analysis focuses on data quality, annual averages, monthly patterns, and visualisation.

Research question

What temporal patterns are present in the supplied county-level malaria incidence dataset?

Tools

- Python
- Pandas
- Matplotlib
- Google Colab / Jupyter Notebook

Methods

- Inspected the dataset's structure and data types.
- Checked for duplicate county-month records and monthly continuity.
- Examined numerical summaries of incidence and environmental variables.
- Calculated annual and calendar-month mean incidence.
- Visualised the time series and temporal summaries.

Preliminary findings

- The dataset contains 6,110 records across 47 counties.
- The annual mean incidence in the supplied data decreases from 14.37 per 1,000 in 2015 to 8.68 per 1,000 in 2025.
- The highest calendar-month mean is observed in June (14.61 per 1,000), while the lowest is observed in December (5.71 per 1,000).

These are descriptive patterns in the supplied dataset, not independently verified estimates of malaria trends in Kenya.

Limitations

The dataset's provenance, measurement methodology, variable definitions, and licence require verification. The analysis does not establish causation or provide validated outbreak forecasts.

Future work

- Verify source documentation and reuse permissions.
- Investigate differences between counties.
- Assess the robustness of temporal patterns.
- Explore baseline forecasting only after validating the data and evaluation design.

Reproducibility

The analysis notebook will be provided in this repository once finalised. The raw dataset is not redistributed here because its reuse permissions have not yet been confirmed.
