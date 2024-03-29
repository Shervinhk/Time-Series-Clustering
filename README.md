# Introduction:
"How can we get the most out of a time series data using longitudinal methods?". This is the main question that this repository attempts to answer. There are various time series analysis methods, however, some are more suitbale for specific data. I will discuss these methods in two broad categories: 

1. **Statistical Methods**: methods that make specific assumptions on the data and take into account the uncertainty of the data. This leads to conclusions that are inherently very intepratible, but some downsides such as if the assumptions are not entirely accurate the results will not be correct.
2. **Machine Learning Methods**: This is the area of unsupervised time series clustering methods. These methods make no specific assumptions on the distribution of the data and attempt to cluster the data based on the learning algorithms.

One of [Frank Harrel's blog posts at Stastical Thinking](https://www.fharrell.com/post/stat-ml/) makes a clear and intriguing distinction between these two which I defintiley recommend reading it. 
However, this ditinction also extends to time series analysis and it's important to know what to use in which setting.
 
I will delve into each of these methods and their differences in specific examples, and make conclusions based on their assumptions.
The main project that I used to work with is not publicly available, however, I will work with a specific dataset that is publicly available and the results can be reproduced. 

This repository is ideal for people who want to understand how to deal with different subpopulations in time series data, and how to get the most out of the data. 

# Complexity of Times Series
There are several underlying complexities with working with time series data such as:
1. **Irregularity in Time Steps**: in most real-world cases the data is not collected in fixed time intervals, therefore it is important to take this into consideration, if possible.
2. **Missing Data**: some time series will have considerable missing data and various approaches can be used to overcome this problem.
3. **Dealing with Outliers**: in some settings, it is important to have good domain knowledge to distinguish between a real outlier and points that are at the edge of the valid range. For instance, in healthcare, some patients who are clinically important might be wrongly excluded because they can be outliers. This is more evident in time series data as there are many subpopulations each with their own valid ranges. 

Because of the aforementioned points, it is important to understand thoroughly what method would work best and would yield the most accurate conclusion with the least amount of confounding.

# Time Series Clustering and Longitudinal Analysis
There are several different methods of time series analysis which are grouped into two major categories:

1. **Longitudinal Analysis**: Models such as Growth Mixture Models (GMM), Latent Class Growth Analysis (LCGA), Fixed and Random Effects Modeling, and AutoRegressive Integrated Moving Average (ARIMA) which the latter one is modelling time series data and the former ones for finding subpopulations and clustering.
2. **Time Series Clustering**: First, finding a distance measure between various time series such as Dynamic Time Warping (DTW) and then using a clustering method such as hierarchical clustering or KMeans. However, as we will elaborate KMeans may not be the ideal approach. Other methods include: Density Based Spatial Clustering (DBSCAN), and k-Shape clustering.

# Pipeline
We will use a specific dataset that we know has several underlying subpopulations and will go through the following pipeline:


1. Preprocessing and preparing the data.
2. Data visulisation to understand the data.
2. Implementation of longitudinal and time series clustering methods.

All of these steps is elaborated in the Jupyter notebook of this repository.



