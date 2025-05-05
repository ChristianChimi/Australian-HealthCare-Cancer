## **Cancer Trends in Australian Public Health**


## **Overview**
This project analyzes cancer-related trends in Australia using historical data from the national public health database. The goal is to uncover insights about cancer incidence and mortality across age, gender, and time, and to build predictive models that support healthcare planning and policy decisions.

[Real Dataset from Australian government site!](https://data.gov.au/dataset/ds-dga-05696f6f-6ff5-42a2-904f-af5e4d1f56f8/details?q=cancer)


## **Pre-processing**
    - Handling Missing Values: Removed rows with missing data for years where cancer information was unavailable.
    - Segmentation: Split the dataset into two separate dataframes—one for cancer Incidence and one for Mortality. Additionally, a specific dataframe for uterine cancer was created.
    - Data Reshaping: Melted and pivoted the uterine cancer dataset by age to prepare it for clustering.

## **Exploratory Data Analysis**
    - I performed exploratory analysis to understand how cancer affects different age groups, genders, and time periods.
        - Cancer Incidence and Mortality by Age: Visualized the trends of cancer incidence and mortality rates across different age groups.
        - Normalized Incidence Plot: Plotted the normalized values of cancer incidence to better compare trends.
        - Death Ratio: Calculated and visualized the death ratio over the years to understand how the mortality rate has evolved.
        - Plotly Interactive visualization:
            - Death rate (mean) for every cancer, descending.
            - Death rate across the years, for every cancer, male and female (select from dropdown).

## **Machine Learning/Statistics**
    - K-Mean:
        - Clustered similar groups by age for uterine cancer.
        - Clustered cancer types by death rate into categories 0, 1, 2. 
    -  MLP:
        - Predicted mortality ratio based on incidence by age group.
        - The model is trained of dataframe from a specific cluster of cancers to improve accuracy, as the death ratio can have huge variety. 
        - The current year is given as input to capture the temporal improvements in cancer treatment and medical advancements over time, improving prediction accuracy.
    - Demonstrated LSTM for predicting incidence rates for Cluster 0 cancers. While the model overfits due to limited data, it would perform better with quarterly data or a larger dataset.
    - Applied ARIMA to predict both mortality and incidence rates for the next five years, providing future insights into cancer trend.

## **Key Insights** 
    - Highest cancer incidence and mortality occur in the 65–69 age group.
    - Uterine cancer incidence is rising faster than its mortality, suggesting early detection or better treatment.
    - Uterine cancer mortality ratio dropped from ~26% in 1985 to ~16% in 2010 — a likely result of medical advancements.
    - Future incidence rates are expected to rise, possibly due to more frequent screenings and awareness campaigns.

## **Conclusions**
This project provides a comprehensive view of cancer trends in Australia, revealing how incidence and mortality vary across age, gender, and time. The combination of exploratory analysis and predictive modeling highlights critical patterns—such as the growing incidence of uterine cancer and the declining mortality ratio—suggesting progress in early detection and treatment. Forecasting models like ARIMA and LSTM offer a forward-looking perspective, supporting proactive healthcare strategies. Overall, the analysis delivers valuable insights to inform public health planning and cancer policy development.



## **Technologies Used**
- **Python**, **Pandas**, **Matplotlib**, **Numpy**, **Pyplot**, **Kmean**, **PyTorch**, **ARIMA**.
 - **Machine Learning for forecasting** and **statistical analysis**
