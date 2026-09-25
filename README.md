<h1>Melbourne Housing Exploratory Data Analysis (EDA) in Python</h1>
<h2>Project Overview</h2>

This project performs Exploratory Data Analysis (EDA) on the Melbourne Housing Dataset using Python in Google Colab. The objective is to analyze the housing data through statistical summaries, data preprocessing, data transformation, and visualizations to gain meaningful insights into property prices and housing characteristics in Melbourne.

<h1>Dataset</h1>

<h3>Dataset Source:</h3>

https://raw.githubusercontent.com/salemprakash/EDA/main/Data/melb_data.csv

The dataset contains information about residential properties sold in Melbourne, Australia, including:

<ol>
    <li>Suburb</li>
    <li>Address</li>
    <li>Number of Rooms</li>
    <li>Property Type</li>
    <li>Property Price</li>
    <li>Sale Method</li>
    <li>Seller Name</li>
    <li>Sale Date</li>
    <li>Distance from CBD</li>
    <li>Postcode</li>
    <li>Number of Bedrooms</li>
    <li>Number of Bathrooms</li>
    <li>Car Parking Spaces</li>
    <li>Land Size</li>
    <li>Building Area</li>
    <li>Year Built</li>
    <li>Council Area</li>
    <li>Latitude</li>
    <li>Longitude</li>
    <li>Region Name</li>
    <li>Property Count</li>
</ol>

<h2>Project Objectives</h2>

<ol>
    <li>Load the Melbourne Housing Dataset</li>
    <li>Perform Basic Statistical Analysis</li>
    <li>Identify and Handle Missing Values</li>
    <li>Clean the Dataset by Removing Duplicates and Invalid Data</li>
    <li>Transform the Data for Better Analysis</li>
    <li>Perform Univariate Analysis Using Visualizations</li>
    <li>Perform Bivariate Analysis Using Visualizations</li>
    <li>Perform Multivariate Analysis Using Visualizations</li>
</ol>

<h2>Technologies Used</h2>

<ol>
    <li>Python</li>
    <li>Google Colab</li>
    <li>Pandas</li>
    <li>NumPy</li>
    <li>Matplotlib</li>
    <li>Seaborn</li>
    <li>Scikit-learn</li>
</ol>

<h2>Analysis Performed</h2>

<h3>Data Preprocessing</h3>
<ol>
    <li>Loaded the Melbourne Housing dataset from GitHub.</li>
    <li>Explored the dataset structure, dimensions, and summary statistics.</li>
    <li>Identified and handled missing values using appropriate techniques.</li>
    <li>Removed duplicate records from the dataset.</li>
    <li>Converted the <code>Date</code> column into <code>datetime</code> format.</li>
    <li>Encoded categorical variables using Label Encoding.</li>
    <li>Normalized the <code>Price</code> column using Min-Max Scaling.</li>
</ol>

<h3>Univariate Analysis</h3>
<ol>
    <li>Histogram of Property Prices</li>
    <li>Boxplot of Property Prices</li>
    <li>Count Plot of Property Types</li>
</ol>

These visualizations help understand the distribution, spread, and frequency of individual variables.

<h3>Bivariate Analysis</h3>

<ol>
    <li>Scatter Plot of Rooms vs Property Price</li>
    <li>Boxplot of Bathrooms vs Property Price</li>
    <li>Bar Plot of Car Parking Spaces vs Property Price</li>
</ol>

These plots illustrate the relationships between two variables and identify possible trends.

<h3>Multivariate Analysis</h3>

<ol>
    <li>Correlation Heatmap of Numerical Features</li>
    <li>Pair Plot of Selected Housing Attributes</li>
    <li>Bubble Plot of Rooms vs Property Price with Bathroom Size</li>
</ol>

These visualizations provide insights into relationships among multiple variables and highlight correlations between housing features.

<h2>Conclusion</h2>

This project demonstrates a complete Exploratory Data Analysis (EDA) workflow using the Melbourne Housing Dataset. It includes data loading, preprocessing, statistical analysis, handling missing values, data cleaning, feature transformation, and various visualization techniques. The analysis helps in understanding property price distributions, relationships among housing attributes, and patterns within the Melbourne housing market. The project serves as a strong foundation for further predictive modeling and machine learning applications in real estate analytics.


<h2>1D Statistical Analysis (Univariate)</h2>

Descriptive Statistics: Calculated Mean, Median, Standard Deviation, Interquartile Range (IQR), Skewness, and Kurtosis.
Distribution Diagnostics: Visualized price distributions and spread using Seaborn Histograms with Kernel Density Estimation (KDE) alongside Boxplots to detect skewness and anomalies.

<h2>2D Statistical Analysis (Bivariate)</h2>

Metrics: Computed Covariance and Pearson Correlation ($r$) between distance to CBD and market price.
Correlation Matrix: Plotted a pairwise correlation heatmap across all numerical attributes.
Linear Trend: Generated regression scatter plots (sns.regplot) evaluating price degradation as distance increases.

<h2>3D Statistical Analysis (Trivariate)</h2>

Spatial Interaction: Constructed a 3D scatter projection using mpl_toolkits.mplot3d.
Feature Mapping: Explored the simultaneous interaction of Distance ($X$), Rooms ($Y$), and Price ($Z$) with a dynamic color gradient.

<h2>K-Means Clustering</h2>

<h3>Feature Standardization: Scaled numerical dimensions using StandardScaler to prevent feature dominance during Euclidean distance calculation.</h3>

<h3>Optimal $k$ Estimation:</h3>
Elbow Method: Measured within-cluster sum of squares (WCSS / Inertia).

Silhouette Analysis: Evaluated cluster cohesion and separation across $k \in [2, 6]$.

<h3>Segmentation: Partitioned properties into distinct market tiers ($k=3$) and visualized cluster boundaries on distance-price planes.</h3>


<h2>Hierarchical (Agglomerative) Clustering</h2>

Linkage Criterion: Applied Ward's minimum variance method (scipy.cluster.hierarchy.linkage) on standardized sub-samples.
Dendrogram Visualization: Plotted hierarchical tree branches with a defined Euclidean cut threshold to isolate distinct housing clusters.
Cluster Assignment: Extracted flat cluster assignments (fcluster) to validate against K-Means groupings.

