# **Cancer Trends in Australian Public Health**
## **Overview**
This project analyzes cancer-related trends in Australia using historical data from the national public health database.

[Real Dataset from Australian government site!](https://data.gov.au/dataset/ds-dga-05696f6f-6ff5-42a2-904f-af5e4d1f56f8/details?q=cancer)

## **Pre-processing**
- Handling Missing Values: Removed rows with missing data.
- Segmentation: Split the dataset into two separate dataframes: one for cancer incidence and one for mortality. 
- Created a dataframe for uterine cancer.
- Data Reshaping: Melted and pivoted the uterine cancer dataset by age (to prepare it for clustering).

## **Exploratory Data Analysis**
 - Visualized the trends of cancer incidence and mortality rates across different age groups.
 - Plotted the normalized values of cancer incidence to compare trends.
 - Calculated and visualized the death ratio over the years to understand the evolving of mortality rate.
 - Plotly Interactive visualization:
   - Death rate for every cancer.
   - Death rate across the years, for every cancer, male and female (with a selection from dropdown).

## **Machine Learning/Statistics**
- K-Mean:
  - Clustered similar groups by age for uterine cancer.
  - Clustered cancer types by death rate into categories 0, 1, 2. 
- xGBoost:
  - Predict cluster from death ratio. Overall good accuracy (70%) but problems with "2" cluster because the dataset is unbalanced (only 5 on 32)
  - Accuracy, Recall, precision, f1 score.
- MLP:
  - Predicted mortality ratio based on incidence by age group.
  - Trained the model on specific clusters of cancer to improve accuracy, as the death ratio of different cancers can be very different. 
  - The current year is given as input to try to capture the temporal improvements in cancer treatment.
- Demonstrated LSTM for predicting incidence rates for Cluster 0 cancers. The model overfits because of limited data, it would perform better with for example quarterly data or a larger dataset.
- Applied ARIMA model to predict both mortality and incidence rates for the next five years.

## **Key Insights** 
- Highest cancer incidence and mortality: 65–69 age group.
- Uterine cancer incidence is rising faster than its mortality, suggesting early detection and/or better treatment.
- Uterine cancer mortality ratio dropped from 26% in 1985 to 16% in 2010. Likely a result of medical advancements.
- Future incidence rates are expected to rise, possibly due to more frequent screenings.

## **Technologies Used**
- **Python**, **Pandas**, **Matplotlib**, **Numpy**, **Pyplot**, **Kmean**, **PyTorch**, **ARIMA**.

## **Conclusions**
The project identified development in cancer medical treatments from 1980 to 2010. Perfomerd also predictive models to forecast incidence and mortality.

