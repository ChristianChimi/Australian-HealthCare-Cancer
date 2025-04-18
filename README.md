Hi! This is a data analysis based on Australian public health database, cancer section.

Steps:
  - First cleaning: drop NaN values for years where we don't hace cancer information.
  - Dividing Dataset into Incidence and Mortality Dataframes.
  - Melt and pivot uterine cancer by age (for clustering)

EDA:
  - Plot of cancer incidence and mortality by age.
  - Plotting normalized values of incidence
  - Calculating and plotting death ratio over the years.

Machine Learning/Statistics:
  - KMean to cluster similar groups by age dor uterine cancer.
  - ARIMA prediction of mortality and incidence for 5 future years
