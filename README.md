Hi! This is a data analysis based on Australian public health database, cancer section.

Dataset source: https://data.gov.au/dataset/ds-dga-05696f6f-6ff5-42a2-904f-af5e4d1f56f8/details?q=cancer

Steps:
  - Pre-processing: drop NaN values for years where we don't have cancer information.
  - Segmentation: Dividing Dataset into Incidence and Mortality Dataframes, also create a different DF for uterine cancer.
  - Data Reshaping: Melt and pivot uterine cancer by age (for clustering)

EDA:
  - Plot of cancer incidence and mortality by age.
  - Plotting normalized values of incidence
  - Calculating and plotting death ratio over the years.
  - Plotly Interactive visualization:
      - Death rate (mean) for every cancer, descending
      - Death rate across the years, for every cancer, male and female (select from dropdown)

Machine Learning/Statistics:
  - KMean:
      - Cluster similar groups by age dor uterine cancer.
      - Cluster type of cancer with similar death rate into 0,1,2 category. 
  - MLP:
      - Use deep learning to predict mortality ratio basing on incidence for every age group.
      - The model is trained of dataframe of a specific cluster of cancers to improve accuracy, as the death ration can have huge variety. 
      - The current year is given as input to capture the temporal improvements in cancer treatment and medical advancements over time, improving prediction accuracy.
  - ARIMA prediction of mortality and incidence for 5 future years
