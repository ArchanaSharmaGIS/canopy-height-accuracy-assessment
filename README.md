
# Canopy Height Accuracy Assessment

This project provides a script to evaluate the accuracy of canopy height predictions against a reference dataset, using ETH Zurich’s Global Canopy Height Map as ground truth data. Key metrics, such as Mean Absolute Error (MAE), Root Mean Square Error (RMSE), Pearson Correlation, and Accuracy Percentage, are calculated to assess the quality of the predictions.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Reference Dataset](#reference-dataset)
3. [Metrics Explanation](#metrics-explanation)
4. [Installation](#installation)
5. [Usage](#usage)
6. [File Structure](#file-structure)
7. [Example Output](#example-output)
8. [Suggested Visuals](#suggested-visuals)
9. [Contributing](#contributing)
10. [License](#license)

## Project Overview

Accurate canopy height mapping is vital for ecological studies, forest management, and carbon stock estimation. This project assesses the accuracy of canopy height model predictions by comparing them to a high-resolution reference dataset, providing error metrics that help quantify the model’s performance.

### Objective

The objective is to help researchers and developers evaluate canopy height models and improve prediction accuracy, supporting more reliable environmental assessments.

## Reference Dataset

The **Global Canopy Height Map** from ETH Zurich serves as the reference data. This dataset provides canopy height estimates at a 30-meter resolution worldwide, derived from multiple data sources. 

*Reference data file used: `reference_canopy_height_ETH_global.tif`*

For more information, visit [ETH Zurich’s Canopy Height Project](https://ethz.ch).

## Metrics Explanation

The following metrics are calculated to provide a comprehensive evaluation of the prediction accuracy:

1. **Mean Absolute Error (MAE)**: Measures the average magnitude of error between predicted and reference values, ignoring direction. A lower MAE indicates a smaller average error, meaning the predictions are closer to the reference.

   \[
   \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} | \text{predicted}_i - \text{reference}_i |
   \]

2. **Root Mean Square Error (RMSE)**: Indicates the standard deviation of prediction errors. Unlike MAE, RMSE penalizes larger errors more heavily, making it sensitive to large deviations.

   \[
   \text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (\text{predicted}_i - \text{reference}_i)^2}
   \]

3. **Pearson Correlation Coefficient**: Measures the linear correlation between predicted and reference values, ranging from -1 (perfect negative correlation) to 1 (perfect positive correlation). A higher correlation value implies that the predictions and reference data follow a similar trend.

   \[
   r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2} \cdot \sqrt{\sum_{i=1}^{n} (y_i - \bar{y})^2}}
   \]

4. **Accuracy Percentage**: Indicates how close the predictions are to the reference data, expressed as a percentage. This is calculated based on the MAE relative to the mean of the reference values.

   \[
   \text{Accuracy Percentage} = 100 - \left(\frac{\text{MAE}}{\text{Mean of Reference Values}} \times 100\right)
   \]

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/YourUsername/canopy-height-accuracy-assessment.git
   cd canopy-height-accuracy-assessment
