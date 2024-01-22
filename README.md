# Hybrid Gini Index Calculation

## Overview

This Jupyter Notebook presents the implementation of the Hybrid Gini Index, a novel approach to calculate Gini Index based on the Lorenz curve of income distribution. The method involves a series of transformations and optimizations to reduce computation time while maintaining accuracy in Gini Index values.

## Gini Index Equation Based on RMSE

The Gini Index equation is derived based on the Root Mean Square Error (RMSE). The equation is expressed as:

\[ Gini = \frac{\sum_{i=1}^{n} (x_i - \bar{x})^2}{2n\bar{x}^2} \]

where \( \bar{x} \) is the mean, \( x_i \) is the data, and \( n \) is the total number of data points.

## Data Preprocessing Steps

1. **Sorting and Shifting Origin**: The income data is sorted in ascending order. Zeros are replaced by a small value (e.g., \(10^{-24}\)) to satisfy the Gini Index equation. Negative values are eliminated by shifting the origin to the least value in the set.

2. **Reducing Computation**: To handle large datasets efficiently, a strategy is employed to reduce the data while maintaining a similar Gini Index value. This involves keeping the 1st and 4th quartiles intact and extracting a percentage of values from the 2nd and 3rd quartiles. This reduces the total number of data points and computation time.

## Observed Differences

The Hybrid Gini Index is compared with the actual Gini Index, and the observed differences are documented. During the initial weeks, the difference ranges between 0.045 and 0.02, reducing to 0.015 after some time, and approaching 0.005 after a year.

## Graphical Representation

The notebook includes a graphical representation of the Hybrid Gini Index compared to the actual Gini Index, illustrating the trend of differences over time.

## Implementation

The code is implemented in a Jupyter Notebook using Python. The notebook provides a step-by-step explanation of the Hybrid Gini Index calculation along with code cells.

## Usage

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/hybrid-gini.git
   cd hybrid-gini
