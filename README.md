# Introduction:
"How can we get the most out of a time series data using longitudinal methods?". This is the main question that this repository attempts to answer. There are various time series analysis methods, however some are more suitbale for a specific data. I will discuss these methods in two broad categories: 

1. **Statstical Methods**: methods that make specific assumptions on the data and take into account the uncertainty of the data. This leads to conclusions that are inherintly very intepratible, but some downsides such as if the assumptions are not entirely accurate the results will not be correct.
2. **Machine Learning Methods**: This is the area of unsuprevised time series clustering methods. These method make no specific assumptions on the distrubtion of the data and attempts to cluster the data based on the learning algorithms.

In one of [Frank Harrel's blog posts at Stastical Thinking](https://www.fharrell.com/post/stat-ml/) makes a clear and intriguing distinction between these two which I defintiley recommend reading it. 
However this ditinction also extends to time series analysis and it's important to know what to use in which setting.
 
I will delve into each of these methods and their differences in specific examples, and make conclusions based on their assumptions.
The main project that I used to work with is not publicly available, however I will work with a specific dataset that is publicly availble and the results can be reproduced. 

This repository is ideal for people who want to understand how to deal with different subpopulations in time series data, and how to get the most out of the data. 

# Complexity of Times Series
There are several underlying complexities with working with time series data such as:
1. **Irregularity in Time Steps**: in most real world cases the data is not collected in fixed time intervals, therefore it is important to take this into consideration, if possible
2. **Missing Data**: some time series will have considerable missing data and various approaches can be used to overcome this problem.
3. **Dealing with Outliers**: in some settings it is important to have a good domain knowledge to distinguish between a real outlier and points that are at the edge of the valid range. For instance, in healthcare some patients who are clinically important might be wrongly excluded because they can be outliers. This is more evident in time series data as there are many subpopulations each with their own valid ranges. 

Because of the afforementioned points, it is important to understand thoroughly what method would work best and would yield the most accurate conclusion with least amount of confcounding.

# Time Series Clustering and Longitudinal Analysis
There are several different methods of time series analysis which are grouped into two major categories:

1. **Longitudinal Analysis**: Models such as Growth Mixture Models (GMM), Latent Class Growth Analysis (LCGA), Fixed and Random Effects Modeling, AutoRegressive Integrated Moving Average (ARIMA), etc.
2. **Time Series Clustering**: First, finding a distance measure between various time series such as Dynamic Time Warping (DTW) and then using a clustering method such as hierchichal clustering or KMeans. However, as we will elaborate KMeans may not be the ideal approach. 

