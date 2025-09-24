# Data-Mining
This project applies data mining and machine learning techniques to explore and predict the health of lobsters caught near the Isle of Skye (2018–2019). The goal was to understand which physical features and environmental factors are most strongly linked to lobster health.  
Dataset Description
 
Source: Lobster data (2018 & 2019) from Isle of Skye.

Format: Excel workbook with two sheets:

Lobster Data 2018

Lobster Data 2019

Size: 4,177 rows × 9 columns (after merging).

Key Columns:

Length(mm), Diameter(mm), Height(mm) → physical size

WholeWeight(g), ShuckedWeight(g), SellWeight(g) → weight indicators

Spots → number of shell spots

Sex → M (male), F (female), I (infant)

Year → 2018 or 2019 (added during preprocessing)

HealthScore → engineered feature (mean of three weights)

🛠️ Technologies Used

Python (Anaconda JupyterLab)

Libraries:

pandas – data wrangling & cleaning

matplotlib, seaborn – visualisations

scikit-learn – regression, clustering, imputation

Machine Learning Models:

Linear Regression (predicting HealthScore)

KMeans Clustering (grouping lobsters by health)

📊 Methods & Workflow
1. Data Understanding & Preprocessing

Loaded Excel sheets and merged them into one dataset.

Added a Year column to distinguish entries.

Removed duplicates and handled missing values with mean imputation.

Encoded Sex (M=0, F=1, I=2).

Engineered HealthScore = average of WholeWeight, ShuckedWeight, SellWeight.

2. Exploratory Data Analysis (EDA)

Descriptive statistics to identify ranges, means, and outliers.

Boxplots to compare HealthScore across sexes and years.

Correlation heatmap to check relationships between features.

3. Predictive Modelling (Linear Regression)

Features: Length, Diameter, Height, weights, Spots.

Train/test split: 70% training, 30% testing.

Missing values handled with SimpleImputer.

Results:

MSE ≈ 0 (1.50 × 10⁻³¹)

R² = 1.0 (perfect fit – features strongly predict HealthScore).

4. Clustering (KMeans)

Features: weight-related columns.

Number of clusters: 2 (higher-health vs lower-health).

Findings:

Cluster 0: mostly infants (lower health).

Cluster 1: mostly adult males & females (higher health).

Slight decline in healthier lobsters in 2019 compared to 2018.

The repository also includes the raw lobster dataset and the Word document of the report for reference.
