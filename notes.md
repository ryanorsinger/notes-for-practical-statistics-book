# Notes for Practical Statistics

## Chapter 1

### Estimates of Location
- arithmetic mean, the regular ol' average
- weighted mean: np.dot(weights, x) / weights.sum()
- trimmed mean: 
	- most robust to outliers
	- dropping a fixed number of high/low values before taking the average
	- lots of means are actually trimmed means if someone removed outliers before taking the mean
	- used in diving scores to reduce the impact of individual impact from judges
	- trimming loses data. That's not always useful or not.
- median
- weighted mean (has its own package called wquantiles)
- trimmed medians exist, too, and are even more robust to outliers, but lose data.
- weighted median
- percentile


### Estimates of Variability aka Dispursion
> Variability, measuring it, reducing it, distinguishing random real variability, and identifying sources of real variability is at the heart of statistics.

- Deviations: difference between observed values and the estimate of location.
- Variance: sum of squared deviations from the mean divided by n-1
- Standard deviation: square root of the variance
- Mean-squared error is another name for variance
- Mean absolute deviation (from the mean):
	- what folks normally think of when they think about deviations
	- Simply: the average distance of all deviations
	- The average of the absolute values of the deviations from the mean
	- L1 norm and Manhattan norm are synonyms for mean absolute deviation
- Mean absolute deviation around the median
- Median absolute deviation from the median
	- The median of the absolute values of deviations from the median
- Range: max_value - min_value
- Percentile: value such that P percent of values take on this value or less and (100-P) percent take on this value or more.
- Interquartile Range: Q3 - Q1
- Order statistics AKA Ranks, metrics based on sorted values








### Exercises
Implement the following functions:
- arithmetic_mean
- weighted_mean
- variance
- mean_square_error
- mean_absolute_deviation
- manhattan_norm
- q3 function to calculate the 75th percentile
- q1 function to calculate the 25th percentile
- iqr to calculate q3 - q1 of a vector of numbers



### Pandas would be cooler if it had a wrapper that did:
- weighted mean, easily accomplished
- harmonic mean
- quadratic mean
- trimmed mean


### Thought pieces
Thought Pieces:
- Consider the list of numbers `[1, 2, 3, 4, 5, 6, 7, 8, 9, 10]`
- What is the middle of this?


## Remember
- L1/manhattan norm is the same as the mean absolute deviation
- L2 norm is the quadratic mean AKA the RMS value 