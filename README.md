# 🌳 Canopy Height Prediction Accuracy Assessment


This project provides a script to evaluate the accuracy of canopy height predictions against a reference dataset, using ETH Zurich’s Global Canopy Height Map as ground truth data. Key metrics, such as Mean Absolute Error (MAE), Root Mean Square Error (RMSE), Pearson Correlation, and Accuracy Percentage, are calculated to assess the quality of the predictions.

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset](#reference-dataset)
3. [Metrics Explanation](#metrics-explanation)
4. [Quantitative Accuracy Metrics for Canopy Height Prediction](#Accuracy-metrics)
5. [Installation](#installation)
6. [Usage](#usage)
7. [File Structure](#file-structure)
8. [Example Output](#example-output)
9. [Suggested Visuals](#suggested-visuals)
10. [Contributing](#contributing)
11. [License](#license)

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

   *Formula:*  
   \[
   \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} | \text{predicted}_i - \text{reference}_i |
   \]

2. **Root Mean Square Error (RMSE)**: Provides a more sensitive error measurement than MAE by penalizing larger errors, giving insights into significant deviations between predicted and reference values.

   *Formula:*  
   \[
   \text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (\text{predicted}_i - \text{reference}_i)^2}
   \]

3. **Pearson Correlation Coefficient (r)**: Assesses the linear relationship between predictions and the reference data. Higher correlation values (closer to ±1) indicate stronger alignment with the reference data trends.

   *Formula:*  
   \[
   r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2} \cdot \sqrt{\sum_{i=1}^{n} (y_i - \bar{y})^2}}
   \]

4. **Accuracy Percentage**: Expresses prediction accuracy relative to the reference dataset as a percentage, where higher values indicate closer alignment.

   *Formula:*  
   \[
   \text{Accuracy Percentage} = 100 - \left(\frac{\text{MAE}}{\text{Mean of Reference Values}} \times 100\right)
   \]

These metrics collectively offer a robust assessment of the model's predictive performance, helping to refine canopy height models for environmental applications.

## Quantitative Accuracy Metrics for Canopy Height Prediction

<img src="/maps/chart_bar.png" alt="Sample Screenshot" width="500">


To evaluate the accuracy of the canopy height predictions, we used the following metrics:

1. Mean Absolute Error (MAE)
Measures the average magnitude of errors between predictions and reference values without considering their direction. A smaller MAE indicates better prediction accuracy.

Formula:

MAE
=
1
𝑛
∑
𝑖
=
1
𝑛
∣
predicted
𝑖
−
reference
𝑖
∣
MAE= 
n
1
​
  
i=1
∑
n
​
 ∣predicted 
i
​
 −reference 
i
​
 ∣
2. Root Mean Square Error (RMSE)
RMSE provides a weighted error measure that penalizes larger discrepancies, highlighting significant deviations between predicted and reference values. Lower RMSE indicates better model performance.

Formula:

RMSE
=
1
𝑛
∑
𝑖
=
1
𝑛
(
predicted
𝑖
−
reference
𝑖
)
2
RMSE= 
n
1
​
  
i=1
∑
n
​
 (predicted 
i
​
 −reference 
i
​
 ) 
2
 
​
 
3. Pearson Correlation Coefficient (r)
Evaluates the linear correlation between predictions and reference data, with values closer to ±1 suggesting a strong positive or negative relationship. It does not account for scale or bias in values but reflects consistency in trends.

Formula:

𝑟
=
∑
𝑖
=
1
𝑛
(
𝑥
𝑖
−
𝑥
ˉ
)
(
𝑦
𝑖
−
𝑦
ˉ
)
∑
𝑖
=
1
𝑛
(
𝑥
𝑖
−
𝑥
ˉ
)
2
⋅
∑
𝑖
=
1
𝑛
(
𝑦
𝑖
−
𝑦
ˉ
)
2
r= 
∑ 
i=1
n
​
 (x 
i
​
 − 
x
ˉ
 ) 
2
 
​
 ⋅ 
∑ 
i=1
n
​
 (y 
i
​
 − 
y
ˉ
​
 ) 
2
 
​
 
∑ 
i=1
n
​
 (x 
i
​
 − 
x
ˉ
 )(y 
i
​
 − 
y
ˉ
​
 )
​
 
4. Accuracy Percentage
Reflects prediction accuracy as a percentage relative to the reference dataset’s mean value. A higher accuracy percentage indicates closer alignment with the reference.

Formula:

Accuracy Percentage
=
100
−
(
MAE
Mean of Reference Values
×
100
)
Accuracy Percentage=100−( 
Mean of Reference Values
MAE
​
 ×100)


## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/YourUsername/canopy-height-accuracy-assessment.git
   cd canopy-height-accuracy-assessment






---

## Table of Contents
1. [Overview](#overview)
2. [About the Reference Dataset](#about-the-reference-dataset)
3. [Evaluation Metrics Explained](#evaluation-metrics-explained)
4. [Installation Guide](#installation-guide)
5. [Running the Code](#running-the-code)
6. [Project Structure](#project-structure)
7. [Sample Output and Visualizations](#sample-output-and-visualizations)
8. [Suggested Visual Captions and Titles](#suggested-visual-captions-and-titles)
9. [Contribution Guide](#contribution-guide)
10. [License](#license)

---

## Overview

Accurate canopy height predictions are essential for analyzing forest structure and biomass, contributing to climate change studies and conservation strategies. This project provides a structured, reproducible framework for assessing the accuracy of canopy height predictions. The results include detailed statistical and error metrics, highlighting areas where canopy height models perform well and where improvements are needed.

---

## About the Reference Dataset

The **Global Canopy Height Map** developed by ETH Zurich serves as the benchmark data. This dataset, built from global remote sensing observations, represents canopy height at a 30-meter resolution and is widely regarded for its high accuracy and consistency.

*Reference data file: `reference_canopy_height_ETH_global.tif`*

Learn more about the reference dataset [here](https://ethz.ch).

---

## Evaluation Metrics Explained

To quantify prediction accuracy, the following metrics are calculated:

1. **Mean Absolute Error (MAE)**: Measures the average error magnitude without regard to direction, providing a straightforward interpretation of error magnitude. Smaller MAE indicates a closer match to the reference.

   *Formula:*  
   \[
   \text{MAE} = \frac{1}{n} \sum_{i=1}^{n} | \text{predicted}_i - \text{reference}_i |
   \]

2. **Root Mean Square Error (RMSE)**: Provides a more sensitive error measurement than MAE by penalizing larger errors, giving insights into significant deviations between predicted and reference values.

   *Formula:*  
   \[
   \text{RMSE} = \sqrt{\frac{1}{n} \sum_{i=1}^{n} (\text{predicted}_i - \text{reference}_i)^2}
   \]

3. **Pearson Correlation Coefficient (r)**: Assesses the linear relationship between predictions and the reference data. Higher correlation values (closer to ±1) indicate stronger alignment with the reference data trends.

   *Formula:*  
   \[
   r = \frac{\sum_{i=1}^{n} (x_i - \bar{x})(y_i - \bar{y})}{\sqrt{\sum_{i=1}^{n} (x_i - \bar{x})^2} \cdot \sqrt{\sum_{i=1}^{n} (y_i - \bar{y})^2}}
   \]

4. **Accuracy Percentage**: Expresses prediction accuracy relative to the reference dataset as a percentage, where higher values indicate closer alignment.

   *Formula:*  
   \[
   \text{Accuracy Percentage} = 100 - \left(\frac{\text{MAE}}{\text{Mean of Reference Values}} \times 100\right)
   \]

These metrics collectively offer a robust assessment of the model's predictive performance, helping to refine canopy height models for environmental applications.

---

## Installation Guide

To get started with this project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/YourUsername/canopy-height-accuracy-assessment.git
   cd canopy-height-accuracy-assessment

