## **Cancer in Australian Health**
This project is a data analysis based on the Australian public health database, specifically focusing on cancer data. The dataset provides insights into cancer incidence and mortality rates across different years, genders, and age groups. The goal is to analyze trends, build predictive models, and gain a deeper understanding of cancer-related statistics in Australia.

Dataset source: https://data.gov.au/dataset/ds-dga-05696f6f-6ff5-42a2-904f-af5e4d1f56f8/details?q=cancer

## **Pre-processing**
    - Handling Missing Values: Removed rows with missing data for years where cancer information was unavailable.
    - Segmentation: Split the dataset into two separate dataframes—one for cancer Incidence and one for Mortality. Additionally, a specific dataframe for uterine cancer was created.
    - Data Reshaping: Melted and pivoted the uterine cancer dataset by age to prepare it for clustering.

## **Exploratory Data Analysis**
    - Cancer Incidence and Mortality by Age: Visualized the trends of cancer incidence and mortality rates across different age groups..
    - Normalized Incidence Plot: Plotted the normalized values of cancer incidence to better compare trends.
    - Death Ratio: Calculated and visualized the death ratio over the years to understand how the mortality rate has evolved.
    - Plotly Interactive visualization:
        - Death rate (mean) for every cancer, descending.
        - Death rate across the years, for every cancer, male and female (select from dropdown).

## **Machine Learning/Statistics**
    - KMean:
        - Cluster similar groups by age dor uterine cancer.
        - Cluster type of cancer with similar death rate into 0,1,2 category. 
    -  MLP:
        - Use deep learning to predict mortality ratio basing on incidence for every age group.
        - The model is trained of dataframe of a specific cluster of cancers to improve accuracy, as the death ration can have huge variety. 
        - The current year is given as input to capture the temporal improvements in cancer treatment and medical advancements over time, improving prediction accuracy.
    - Demonstrated LSTM for predicting incidence rates for Cluster 0 cancers. While the model overfits due to limited data, it would perform better with quarterly data or a larger dataset.
    - Applied ARIMA to predict both mortality and incidence rates for the next five years, providing future insights into cancer trend.

## **Technologies Used**
- **Python**, **Pandas**, **Matplotlib**, **Numpy**, **Pyplot**, **Kmean**, **PyTorch**, **ARIMA**.
 - **Machine Learning for forecasting** and **statistical analysis**
