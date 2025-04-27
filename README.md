# Wine Quality Clustering Analysis-Data Mining

## Project Overview
This project applies clustering techniques to a dataset containing physicochemical properties of white wine samples to discover hidden patterns and natural groupings among the wines. The analysis focuses on segmenting wines based on their quality-related attributes using **unsupervised learning**.

## Methods Used
- **Exploratory Data Analysis (EDA)**
- **Data Standardization** (using `StandardScaler`)
- **KMeans Clustering**
- **Elbow Method** (to determine the optimal number of clusters)
- **Principal Component Analysis (PCA)** for 2D Visualization
- **Cluster Interpretation**

## Dataset Information
- **Name:** Wine Quality — White Wine
- **Source:** UCI Machine Learning Repository
- **Rows:** 4898
- **Features:**
  - `fixed acidity`, `volatile acidity`, `citric acid`, `residual sugar`, `chlorides`, 
  - `free sulfur dioxide`, `total sulfur dioxide`, `density`, `pH`, `sulphates`, 
  - `alcohol`, `quality` (score between 0 and 10)

The dataset includes various physicochemical tests of white wines and their quality ratings given by wine tasters.

##  Project Workflow
1. **Data Loading & Preprocessing**
   - Loaded the CSV file into a Pandas DataFrame.
   - Checked for missing values and data types.
   - Selected relevant features for clustering (excluding target `quality` for unsupervised learning).
   - Scaled features using **StandardScaler** for uniformity.

2. **Finding Optimal Clusters**
   - Applied the **Elbow Method** using the Within-Cluster-Sum-of-Squares (WCSS) to determine the best number of clusters.
   - Observed the "elbow point" to be at **3 clusters**.

3. **Model Building**
   - Built a **KMeans Clustering** model with 3 clusters.
   - Assigned cluster labels to the original data.

4. **Visualization**
   - Reduced dimensions using **Principal Component Analysis (PCA)**.
   - Visualized the clusters in a 2D scatter plot colored by cluster assignment.

5. **Insights & Interpretation**
   - Each cluster showed distinct characteristics in terms of alcohol content, acidity, and quality.
   - Helped understand different groups of wines based on their chemical makeup.

## Key Visualizations
- **Elbow Plot:** To identify the optimal number of clusters.
- **PCA Scatter Plot:** To visualize the clustering of wine samples in two dimensions.

## Outcomes
- Identified **3 distinct groups** among white wines based on chemical properties.
- Learned that wines with higher alcohol and balanced acidity tended to form a separate, often higher-quality cluster.
- Demonstrated the usefulness of clustering techniques in unsupervised pattern discovery.

## Libraries Used
- Python 3.x
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-Learn (for scaling, clustering, and PCA)

## How to Run
1. Clone the repository.
2. Install dependencies:  
   ```bash
   pip install -r requirements.txt
