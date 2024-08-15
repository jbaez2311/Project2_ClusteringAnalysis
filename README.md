# K-Means Clustering Analysis of University Data

## Table of Contents
1. [Overview](#overview)
2. [Files](#files)
3. [Project Structure](#project-structure)
   - [Executive Summary](#executive-summary)
   - [Data Description](#data-description)
   - [Steps of Analysis](#steps-of-analysis)
     1. [Data Import and Initial Glimpse](#data-import-and-initial-glimpse)
     2. [Data Profiling](#data-profiling)
     3. [Handling Missing Values](#handling-missing-values)
     4. [Data Normalization](#data-normalization)
     5. [K-Means Clustering](#k-means-clustering)
     6. [Final Clustering and Label Assignment](#final-clustering-and-label-assignment)
     7. [Heatmap Visualization](#heatmap-visualization)
   - [Cluster Descriptions](#cluster-descriptions)
4. [Conclusion](#conclusion)
5. [How to Use](#how-to-use)

## Overview
This project applies an unsupervised learning technique, specifically K-Means clustering, to categorize universities into distinct groups based on various features such as application numbers, enrollment rates, expenditure, and student-to-faculty ratios. The analysis aims to uncover inherent patterns in the data that differentiate universities from one another.

## Files
- **University_Data.csv**: The dataset containing information about various universities, including attributes such as the number of applications received, acceptance rates, graduation rates, and more.
- **K-Means Analysis.pdf**: A PDF export of the Jupyter notebook that documents the step-by-step analysis conducted on the university data, including data cleaning, clustering, and results interpretation.

## Project Structure

### Executive Summary
The goal of this project is to use K-Means clustering to understand the differences among universities by grouping them into clusters based on similar attributes.

### Data Description
The dataset contains the following columns:
- `University_Name`: The name of the university.
- `Private`: Indicates whether the university is private (Yes) or public (No).
- `Apps`: Number of applications received.
- `Accept`: Number of applications accepted.
- `Enroll`: Number of new students enrolled.
- `Top10perc`: Percentage of new students from the top 10% of their high school class.
- `Top25perc`: Percentage of new students from the top 25% of their high school class.
- `F.Undergrad`: Number of full-time undergraduates.
- `P.Undergrad`: Number of part-time undergraduates.
- `Outstate`: Out-of-state tuition cost.
- `Room.Board`: Room and board costs.
- `Books`: Estimated book costs.
- `Personal`: Estimated personal expenses.
- `PhD`: Percentage of faculty with Ph.D. degrees.
- `Terminal`: Percentage of faculty with terminal degrees.
- `S.F.Ratio`: Student-to-faculty ratio.
- `perc.alumni`: Percentage of alumni who donate.
- `Expend`: Instructional expenditure per student.
- `Grad.Rate`: Graduation rate.

### Steps of Analysis
#### 1. Data Import and Initial Glimpse
The dataset is imported and a preliminary overview is conducted to understand the data structure and content.

#### 2. Data Profiling
A comprehensive data profiling report is generated to assess the quality of the data, including identifying missing values.

#### 3. Handling Missing Values
Missing values in the dataset are imputed using the mean of the respective columns to avoid skewing the data distribution.

#### 4. Data Normalization
The data is normalized to ensure that all features contribute equally to the clustering process and to improve the convergence of the K-Means algorithm.

#### 5. K-Means Clustering
Various cluster sizes are tested using the silhouette score to determine the optimal number of clusters. It is found that three clusters yield the best silhouette score.

#### 6. Final Clustering and Label Assignment
The dataset is re-clustered using the optimal number of clusters, and cluster labels are assigned to each university.

#### 7. Heatmap Visualization
A heatmap is generated to visualize the mean values of each feature within the clusters, helping to interpret the characteristics of each cluster.

### Cluster Descriptions
- **Cluster 0**: Represents larger universities with higher application numbers and expenditures but lower graduation rates and student-faculty ratios.
- **Cluster 1**: Consists of selective and academically prestigious institutions with higher percentages of top-performing students and faculty with advanced degrees.
- **Cluster 2**: Contains smaller universities with strong student-faculty engagement and high alumni donation rates but lower selectivity and graduation rates.

## Conclusion
The analysis successfully categorized universities into distinct clusters, each with unique characteristics. These insights can be used for further analysis or decision-making regarding university policies or strategies.

## How to Use
1. **Data Preparation**: Ensure that the `University_Data.csv` file is in the same directory as the analysis script.
2. **Running the Analysis**: Open the Jupyter notebook (if available) and run all cells to reproduce the analysis. Alternatively, refer to the `K-Means Analysis.pdf` for the complete documentation of the process.
3. **Interpreting Results**: Review the clustering results and heatmap visualizations to understand the key characteristics of each university cluster.
