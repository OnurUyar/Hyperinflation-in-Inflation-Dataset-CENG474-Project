# Hyperinflation in Inflation Dataset CENG474-Project
The project we did with my teammate at the end of the 5th semester for CENG 474 (Introduction to Data Science) course.  

In this project, we used the 5 main inflation types (Headline Consumer Price, Energy Consumer Price, Food Consumer Price, Official Core Consumer Price, Producer Price) data from 1970 to 2022 of all countries in the world that share their inflation data, which we found readily available on the internet (global_dataset_inflation.csv).

Our aim is to make the incomplete, inaccurate and inconsistent data sets we find on the internet cleaner, more consistent and workable by using the functions and methods we learned in the CENG 474 Introduction to Data Science course and find countries in the data set that are or are not in _**hyperinflation**_.

Which methods we used and what results they gave are written in the main file (main.ipynb). We evaluated data quality by deleting unnecessary data in the data set and replacing empty and inconsistent values with the average values of that country.

However, the data set we use is time dependent and since there is no connection between these data, we experienced problems while using some methods:

-- _**PCA:**_ PCA functions does not accept our datas from the dataset and causes error.  
-- _**CHI Squared:**_ Since there is no correlation between inflation data, we cannot use the CHI Squared function.  
-- _**Recursive Feature Elimination:**_ RFE functions does not accept non-negative values.  
-- _**Singular Value Decomposition:**_ It is not appropriate to apply SVD to time-dependent data sets because these data sets often contain time components and therefore cannot be treated as a flat matrix.  
-- _**Linear Combinations:**_ Time-dependent data sets have random fluctuations. These random fluctuations cannot be predicted and modeled with a linear combination.  
-- _**Sampling Data:**_ Since our data set is time dependent and there is no connection between them, sampling samples cannot give consistent results.  
-- _**Generate Synthetic Data (SMOTE):**_ Synthetic Minority Over-sampling Technique (SMOTE) cannot be used in time-dependent data sets.  
-- _**K-fold Cross Validation:**_ K-fold cross-validation does not take into account time series features as it randomly splits the data set, which impairs the real-world performance of the model.

This data set can be made more meaningful and consistent with Long Short-Term Memory (LSTM) models, which we did not learn while doing the project and which was the topic of the last week.
