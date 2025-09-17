# README: Removing Outliers Using Z-Score and IQR Methods

## Objective
The objective of this experiment is to demonstrate two common methods for identifying and removing outliers from a dataset: the Z-score method and the Interquartile Range (IQR) method. Outliers can significantly skew statistical analyses and machine learning models, so it is essential to detect and handle them appropriately.

## Problem Statement
Outliers are data points that deviate significantly from other observations in a dataset. They can arise due to measurement errors, data entry mistakes, or genuine variability. This experiment aims to:
1. Identify outliers in a given dataset using the Z-score and IQR methods.
2. Compare the effectiveness of these methods in detecting outliers.
3. Visualize the dataset with outliers using a box plot.

## Dataset Used and Its Description
The dataset used in this experiment is a simple list of numerical values:
```
[2, 4, 5, 6, 12, 15, 100]
```
- **Description**: The dataset contains 7 data points, with the value `100` being a potential outlier due to its significant deviation from the other values.

## Methods Used to Solve the Problem
1. **Z-Score Method**:
   - The Z-score measures how many standard deviations a data point is from the mean.
   - Data points with a Z-score greater than a specified threshold (typically 3) are considered outliers.
   - In this experiment, no outliers were detected using a threshold of 3.

2. **Interquartile Range (IQR) Method**:
   - IQR is the range between the first quartile (25th percentile) and the third quartile (75th percentile).
   - Outliers are defined as data points below `Q1 - 1.5 * IQR` or above `Q3 + 1.5 * IQR`.
   - In this experiment, the value `100` was identified as an outlier using the IQR method.

3. **Visualization**:
   - A box plot was used to visualize the dataset and highlight the outliers.

## Results
- **Z-Score Method**:
  - Z-scores: `[-0.57, -0.51, -0.48, -0.45, -0.26, -0.17, 2.43]`
  - Outliers detected: `None` (using a threshold of 3).

- **IQR Method**:
  - Q1: `4.5`, Q3: `13.5`, IQR: `9.0`
  - Lower Bound: `-9.0`, Upper Bound: `27.0`
  - Outliers detected: `[100]`

- **Box Plot**:
  - The box plot clearly shows the outlier `100` as a point outside the upper whisker.

## Conclusion
- The Z-score method did not detect any outliers in this dataset when using a threshold of 3, while the IQR method successfully identified `100` as an outlier.
- The choice of method depends on the dataset and the context. The Z-score method is sensitive to the mean and standard deviation, making it less robust for small datasets or those with extreme outliers. The IQR method, being based on percentiles, is more robust for such cases.
- Visualization tools like box plots are highly effective for identifying outliers and understanding the distribution of data.

