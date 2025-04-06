# Customer Segmentation Project using Mall_Customers Data

This project performs customer segmentation using the `Mall_Customers` dataset. It applies clustering techniques to group customers based on their purchasing behavior and demographic features.

## Features

- **Data Upload**: Uploads a CSV file containing customer data.
- **Data Overview**: Displays data information and descriptive statistics.
- **Preprocessing**: Prepares the data by standardizing features and encoding categorical variables.
- **Dimensionality Reduction**: Uses PCA to reduce dimensions while retaining a specified variance threshold.
- **Clustering**: Applies DBSCAN clustering to group customers.
- **Cluster Analysis**: Summarizes clusters with key metrics such as average age, income, and spending score.
- **Visualization**:
  - K-distance graph for determining optimal DBSCAN parameters.
  - Scatter plot of clusters in PCA-reduced space.
  - Feature distributions segmented by clusters.

## Requirements

- Python 3.x
- Required libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `scikit-learn`
  - `google.colab` (if running on Google Colab)

## How to Run

1. **Install Dependencies**:
   Install the required Python libraries using pip:
   ```bash
   pip install pandas numpy matplotlib scikit-learn
   ```

2. **Upload Data**:
   Use the `upload_file()` function to upload the `Mall_Customers.csv` file. Ensure the file contains the following columns:
   - `CustomerID`
   - `Gender`
   - `Age`
   - `Annual Income (k$)`
   - `Spending Score (1-100)`

3. **Run the Notebook**:
   Execute the cells in the Jupyter Notebook or Google Colab in sequence to perform the analysis.

4. **Adjust Parameters**:
   - Use the K-distance graph to determine the optimal `eps` for DBSCAN.
   - Modify `min_samples` as needed for better clustering results.

5. **Output**:
   - Cluster labels will be added to the original DataFrame.
   - Key metrics for each cluster will be displayed.
   - Visualizations will help interpret the clustering results.

## Key Functions

- `upload_file()`: Uploads a CSV file and returns a DataFrame.
- `data_overview(df)`: Displays data information and descriptive statistics.
- `preprocess_data(df)`: Preprocesses the data by standardizing and encoding features.
- `optimal_pca(scaled_features, variance_threshold)`: Reduces dimensions using PCA.
- `find_optimal_eps(reduced_data)`: Visualizes the K-distance graph for DBSCAN.
- `perform_dbscan(reduced_data, eps, min_samples)`: Performs DBSCAN clustering.
- `cluster_analysis(df)`: Summarizes clusters with key metrics.
- `generate_feedback(cluster_summary, df)`: Generates insights for each cluster.
- `plot_cluster_scatter(reduced_data, df)`: Visualizes clusters in PCA-reduced space.
- `plot_feature_distributions(df)`: Plots feature distributions segmented by clusters.

## Visualization

- **K-distance Graph**: Helps determine the optimal `eps` for DBSCAN.
- **Cluster Scatter Plot**: Displays clusters in PCA-reduced space.
- **Feature Distributions**: Shows histograms of features segmented by clusters.

## License

This project is licensed under the MIT License. See the `LICENSE` file for details.
