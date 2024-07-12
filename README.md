# Customser segmentation using K-means

## Introduction

### Project Overview
This project focuses on utilizing machine learning techniques, specifically K-Means clustering, for customer segmentation in a retail setting. The primary goal is to identify distinct groups of customers based on their purchasing behavior. By segmenting customers, businesses can tailor marketing strategies, improve customer retention, and optimize product offerings to better meet the diverse needs of different customer segments.

### Purpose
The purpose of this project is twofold:
1. **Segmentation:** To divide customers into meaningful groups based on their purchasing patterns and behaviors.
2. **Insights:** To derive actionable insights from the segmentation that can inform marketing campaigns, product recommendations, and overall business strategy.

### Goals
- Apply K-Means clustering algorithm to segment customers using transactional data.
- Evaluate the effectiveness of the segmentation through metrics like silhouette score.
- Interpret and visualize the results, customer engagement, and retention rates for each segment.

## Dataset Description

### Source
The dataset used in this project was sourced from [Kaggle](https://www.kaggle.com/datasets/ravalsmit/customer-segmentation-data).

### Key Attributes
- **Customer ID:** Unique identifier for each customer.
- **Age:** Age of the customer.
- **Gender:** Gender of the customer.
- **Marital Status:** Marital status of the customer.
- **Education Level:** Highest education level attained by the customer.
- **Geographic Information:** Location of the customer.
- **Occupation:** Job or profession of the customer.
- **Income Level:** Income level of the customer.
- **Behavioral Data:** Behavioral insights about the customer.
- **Purchase History:** Date of last purchase by the customer.
- **Interactions with Customer Service:** Preferred method of communication.
- **Insurance Products Owned:** Types of insurance policies owned by the customer.
- **Coverage Amount:** Insurance coverage amount.
- **Premium Amount:** Insurance premium amount.
- **Policy Type:** Type of insurance policy.
- **Customer Preferences:** Preferences of the customer regarding various aspects.
- **Preferred Communication Channel:** Preferred method of communication.
- **Preferred Contact Time:** Preferred time for contact.
- **Preferred Language:** Language preferred by the customer.
- **Segmentation Group:** Segment to which the customer belongs.

### Relevance to Customer Segmentation
- **Demographics:**
  - **Age:** Essential for segmenting based on life stage and preferences.
  - **Gender:** Helps tailor marketing strategies and product offerings.
  - **Marital Status:** Influences buying behavior and needs, particularly for insurance products.
  - **Education Level:** Higher education levels may correlate with different financial behaviors and product needs.
- **Geographic Information:**
  - **Location:** Helps in understanding regional preferences and tailoring localized marketing strategies.
- **Occupation and Income:**
  - **Occupation:** Different occupations may have varying risk profiles and product needs.
  - **Income Level:** Higher-income individuals may prefer different products and services compared to lower-income segments.
- **Behavioral Data:**
  - **Purchase History:** Indicates future buying behavior and product preferences.
  - **Interactions with Customer Service:** Enhances customer experience and satisfaction.
- **Insurance Products:**
  - **Insurance Products Owned:** Helps in cross-selling and up-selling relevant products.
  - **Coverage and Premium Amount:** Helps in creating more tailored insurance plans.
- **Customer Preferences:**
  - **Preferred Communication Channel:** Improves engagement and response rates.
  - **Preferred Contact Time:** Enhances communication effectiveness.
  - **Preferred Language:** Improves customer satisfaction and loyalty.
- **Segmentation Group:** Identifies which segment each customer belongs to, allowing for targeted marketing and personalized offerings.

## Methodology

### 1. Data Upload and Initial Inspection
First, the dataset `Vishwa.csv` was uploaded, and the initial few rows were inspected to understand its structure and content.

### 2. Data Preprocessing
- **Encoding Categorical Variables:** The categorical variables 'Gender' and 'Marital_Status' were encoded using LabelEncoder.
- **Standardization:** The entire dataset was standardized using StandardScaler to ensure that each feature contributes equally to the clustering process.

### 3. Clustering with K-Means
- **Initial Clustering:** The K-Means clustering algorithm was applied to the standardized data with an initial choice of 33 clusters. The model was evaluated using the inertia and silhouette score metrics.
- **Optimal Number of Clusters:** A range of clusters from 2 to 99 was evaluated using silhouette scores to determine the optimal number of clusters. The number of clusters with the highest silhouette score was selected as the optimal number.
- **Re-evaluation:** The K-Means model was retrained using the optimal number of clusters. Cluster labels were predicted for each data point, and the model was re-evaluated using inertia and silhouette scores. Cluster centers and sizes were also documented.

### 4. Visualization
- **PCA Visualization:** Principal Component Analysis (PCA) was used to reduce the data to 2 dimensions for visualization. A scatter plot of the PCA-reduced data was created to visualize the clusters.
- **Cluster Visualization:** The clusters were visualized using scatter plots of 'Gender' vs 'Income'. Separate plots were created for the training and validation sets to ensure model consistency. Cluster centers were highlighted in the plots.

### 5. Model Validation
- **Training and Validation Split:** The data was split into training and validation sets. The K-Means model was trained on the training set and evaluated on both the training and validation sets using silhouette scores.

### 6. Gender and Income Analysis
- **Optimal Clustering:** The optimal number of clusters for 'Gender' and 'Income' was determined using the silhouette score. The K-Means model was applied to the subset of data containing 'Gender' and 'Income'.
- **Income Analysis:** A function was defined to calculate the average income based on gender and age range. The function was tested for various age ranges, and the results were plotted.

### 7. Visualization Enhancements
- **Bar Chart Enhancements:** A bar chart was created to visualize the average income of females in different age ranges. The chart was enhanced with gradient colors, data labels, shadows for a 3D effect, and grid lines for better readability. Titles and labels were added with different fonts and weights for improved presentation.

## Summary of Customer Segmentation Project

### Results
The analysis resulted in the identification of distinct customer segments, each characterized by unique behaviors and attributes. Key segments included high-value customers, price-sensitive customers, and occasional buyers. Insights from the segmentation analysis were used to propose targeted marketing strategies and personalized customer engagement plans.

### Conclusion
The customer segmentation project provided valuable insights into the diverse customer base. By understanding the different segments, the business can implement more effective marketing campaigns, improve customer satisfaction, and drive higher revenue.

### Future Work
- Continuous monitoring and updating of customer segments to reflect changing behaviors and trends.
- Integration of additional data sources such as social media interactions and customer feedback to enrich the segmentation analysis.
- Application of advanced techniques like deep learning for more nuanced segmentation.
