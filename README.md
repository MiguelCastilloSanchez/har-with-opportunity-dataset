# Human Activity Recognition using Opportunity Dataset

This repository contains all the code and information for the human activity recognition project using the Opportunity dataset. The project aims to improve the accuracy and robustness of human activity recognition by fusing data from multiple sensors.

## Table of Contents

* [Introduction](#introduction)
* [Dataset](#dataset)
* [Methodology](#methodology)
* [Results](#results)
* [Conclusion](#conclusion)
* [References](#references)


## Introduction

Human Activity Recognition (HAR) is a crucial research area in artificial intelligence and ubiquitous computing. This project focuses on improving HAR by leveraging data fusion techniques on the Opportunity dataset, which contains rich sensor data captured in a realistic environment simulating daily morning activities.


## Dataset

The Opportunity dataset includes recordings from subjects performing various activities in a sensor-rich environment. The dataset includes data from 72 sensors across 10 modalities, including accelerometers, gyroscopes, and object interaction sensors. For this project, a subset of the dataset focusing on simple human activities (standing, walking, sitting, lying) was used. These activities can be identified solely using on-body sensors, which simplifies the data processing and allows for a more focused analysis.


## Methodology

The methodology involved several steps:

1. **Data Loading and Preprocessing:** The data was loaded and preprocessed to handle missing values, scale features, and segment data into 3-second windows. This windowing technique facilitates feature extraction and makes the dataset more manageable while retaining relevant information.

2. **Feature Extraction:** Twelve statistical features were extracted from each sensor, including mean, standard deviation, maximum value per axis, mean magnitude, standard deviation of the magnitude, and area under the curve of the magnitude.

3. **Feature Selection:** Analysis of Variance (ANOVA) was used to select the most relevant features for classification, reducing the dimensionality and improving model efficiency.

4. **Dimensionality Reduction:** Linear Discriminant Analysis (LDA) was employed to further reduce the dimensionality while maximizing class separability.

5. **Classification and Fusion:** Three classifiers (Logistic Regression, Random Forest, and Perceptron) were trained and evaluated. Additionally, three data fusion methods (Aggregation with Random Forest, Voting with Logistic Regression, Random Forest, and Naive Bayes, and AdaBoost) were implemented and compared.

6. **Evaluation:** Cross-validation was used to evaluate the performance of both individual classifiers and fusion models.  Metrics such as accuracy, precision, recall, and F1-score were used for performance assessment.


## Results

The results showed that all models, including those without data fusion, achieved accuracy above 93%. However, the data fusion models consistently outperformed the single classifier models across all metrics. This highlights the effectiveness of data fusion for improving HAR. Among the fusion methods, there were minor performance differences, indicating the need to select an appropriate fusion technique based on the specific application requirements.

## Conclusion

This project demonstrated the value of data fusion techniques for enhancing human activity recognition. The results support the hypothesis that fusion improves performance compared to traditional single-classifier approaches. Further research could explore other data fusion methods and investigate the computational cost associated with each technique to optimize the trade-off between performance and efficiency.

## References

The relevant references for the methodologies and datasets used are included in the project report. Please refer to the report for a complete list of citations.
