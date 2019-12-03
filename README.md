# Multivariate Phase 1 Analysis for Monitoring Manufacturing Process

Objective of this project is to identify the in-control data points and eliminate out of control data points to set up distribution parameters for the future monitoring of manufacturing process.

## Executive Summary

The objective of the project is to identify the in-control distribution parameters of the given dataset. The dataset is obtained from a manufacturing process which has 209 variables and 552 data points. It contains both in-control and out-of-control data points. While the physical interpretation of the variables is not specified. our focus is mainly based on eliminating the outof-control data points using multivariate control charts so that a control scheme can be set up for monitoring the future data points. This approach is essentially known as Phase I Analysis of Multivariate data.

As the number of variables in the dataset is large, firstly we used dimension reduction methods to reduce the dimension of the whole dataset. Principal Component Analysis (PCA) was used to reduce the dimension by which we obtained 4 PCs which explain the 80.097 % variability from the original dataset. The covariance matrix was used for PCA as the physical interpretation of
variables has been omitted, the relative magnitude between them might be of importance.

Once we have the Principal Components, then Multivariate charts like Hotelling T2 Chart and mCUSUM charts were used to detect and eliminate the out-of-control points within the dataset. Firstly, to eliminate large spikes within dataset, we applied T2 chart on the transformed variables till we got zero out-of-control data points. Then, to account for the small sustained mean shift, we used m-CUSUM charts. Multiple iterations were required of both the control charts to clean the data of any outliers that were present.

Finally, the distribution parameters can be set up using the cleaned data set and which can be used for monitoring future data. We used packages within R software as a tool for computational work.
