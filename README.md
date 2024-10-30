# 🌳 Canopy Height Prediction Accuracy Assessment


This project provides a script to evaluate the accuracy of canopy height predicti  
ons against a reference dataset, using ETH Zurich’s Global Canopy Height Map as ground truth data. Key metrics, such as Mean Absolute Error (MAE), Root Mean Square Error (RMSE), Pearson Correlation, and Accuracy Percentage, are calculated to assess the quality of the predictions.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Objective](#objective).
3. [Dataset](#dataset)
4. [Metrics Explanation](#metrics-explanation)
5. [Quantitative Accuracy Metrics for Canopy Height Prediction](#Quantitative-Accuracy-Metrics-for-Canopy-Height-Prediction)
6. [Model Performance Summary](#Model-Performance-Summary)


## Project Overview

Accurate canopy height mapping is vital for ecological studies, forest management, and carbon stock estimation. This project assesses the accuracy of canopy height model predictions by comparing them to a high-resolution reference dataset, providing error metrics that help quantify the model’s performance.

## Objective
Accurate canopy height predictions are essential for analyzing forest structure and biomass, contributing to climate change studies and conservation strategies. This project provides a structured, reproducible framework for assessing the accuracy of canopy height predictions. The results include detailed statistical and error metrics, highlighting areas where canopy height models perform well and where improvements are needed.


## Dataset

In this project, canopy height was predicted using a machine learning model trained on various remote sensing datasets. The model enhances prediction accuracy by leveraging features from satellite imagery. The comparison of the predicted canopy heights against the ETH Zurich dataset allows for a thorough assessment of the model's performance and effectiveness in estimating canopy heights.

For more information, visit [ETH Zurich’s Canopy Height Project](https://ethz.ch).<br><br>

<img src="/maps/pre_canopyheight.png" alt="Sample Screenshot" width="500">
<img src="/maps/refer_canopyheight.png" alt="Sample Screenshot" width="500">







## Metrics Explanation
To quantify prediction accuracy, the following metrics are calculated:

1. **Mean Absolute Error (MAE)**: Measures the average error magnitude without regard to direction, providing a straightforward interpretation of error magnitude. Smaller MAE indicates a closer match to the reference.

        MAE = (1 / n) * Σ | predicted_i - reference_i |


2. **Root Mean Square Error (RMSE)**: Provides a more sensitive error measurement than MAE by penalizing larger errors, giving insights into significant deviations between predicted and reference values. Lower RMSE indicates better model performance.

       RMSE = sqrt((1 / n) * Σ (predicted_i - reference_i)^2) 

  
4. **Pearson Correlation Coefficient (r)**: Assesses the linear relationship between predictions and the reference data. Higher correlation values (closer to ±1) indicate stronger alignment with the reference data trends.

       r = Σ((x_i - x̄)(y_i - ȳ)) / sqrt(Σ(x_i - x̄)^2 * Σ(y_i - ȳ)^2)


5. **Accuracy Percentage**: Expresses prediction accuracy relative to the reference dataset as a percentage, where higher values indicate closer alignment.

       Accuracy Percentage = 100 - (MAE / Mean of Reference Values * 100)


These metrics collectively offer a robust assessment of the model's predictive performance, helping to refine canopy height models for environmental applications.

## Quantitative Accuracy Metrics for Canopy Height Prediction

<img src="/maps/chart_bar.png" alt="Sample Screenshot" width="500">

## Model Performance Summary
The current model performance, based on the comparison with ETH Zurich’s Global Canopy Height Map as reference data, is summarized below:

#### Interpretation of Results
MAE (6.90) and RMSE (8.71) suggest there are notable errors between the predicted canopy heights and the reference values. While these values show the model captures some canopy height variation, they also highlight areas for improvement.<br>
Pearson Correlation (0.70) indicates a moderate linear relationship between predicted and reference canopy heights. This suggests that the model captures some trends in canopy height but may not fully reflect actual canopy variations.<br>
Accuracy Percentage (61.07%) shows that the model captures approximately 61% of the canopy height variation. This lower percentage is due to limitations in input data quality, which impacts the accuracy of the predictions.<br>

<img src="/maps/matric.png" alt="Sample Screenshot" width="500">
