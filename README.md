<p align="center">
<img src="https://github.com/user-attachments/assets/bc3bd6c7-fd6e-4f50-8c49-690cc5dc8bd5" height="50%" width="50%" alt="drug-classification"/>
</p>

# Cardiovascular Drug Classification With SPSS

This project involves classifying unknown cardiovascular drugs based on various metrics collected from a dataset of 200 individuals using IBM SPSS Statistics.<br />

## Video Demonstration

- ### [YouTube: Classifying Unknown Drugs with SPSS](https://www.youtube.com/watch?v=e-RB83Nz74c)

## Environments and Technologies Used

- IBM SPSS Statistics
- Kaggle Cardiovascular Dataset: [Here](https://www.kaggle.com/code/matinmahmoudi/drug-classification-quick-start-for-beginners/input)
- Operating System: Windows 11

## High-Level Deployment and Configuration Steps

- **Step 1:** Data Acquisition: Download the cardiovascular dataset from Kaggle.
- **Step 2:** Data Import: Import the CSV file into IBM SPSS Statistics, ensuring that the first row contains headers.
- **Step 3:** Data Preprocessing: Perform data cleaning, handle missing values, and encode categorical variables.
- **Step 4:** Model Development: Apply various classification algorithms and evaluate their performance.
- **Step 4:** Model Deployment: Save and document the best-performing model for future use.

# Exploring the Data

## Importing the CSV in SPSS
<p align="center">
  <img src="https://github.com/user-attachments/assets/9f74af65-964a-45de-b885-0858b4d83361" height="80%" width="80%" alt="SPSS Overview"/>
</p>
<p>
  
- Open IBM SPSS Statistics.

- Navigate to File > Open > Data.

- Select the downloaded CSV file from Kaggle.

- Ensure that the option "Read variable names from the first row of data" is checked.

- Click OK to import the data.
</p>
<br />

## Examining Numerical and Classification Distributions
<p align="center">
  <img src="https://github.com/user-attachments/assets/490d3590-7abc-4974-a3be-c92c1de89415" height="80%" width="80%" alt="Descriptive and Frequentist Statistics"/>
  <img src="https://github.com/user-attachments/assets/038987e3-7733-4747-b909-567cf0940111" height="80%" width="80%" alt="Overview of Data"/>
</p>
<p> 

- Numerical Variables:

    - Analyze the distribution of each numerical feature to identify outliers, skewness, or anomalies.
      
    - Utilize descriptive statistics such as mean, median, standard deviation, and visualizations like histograms.

- Categorical Variables:

    - Examine the distribution of categorical variables using bar plots to ensure a balanced representation across classes.
</p>
<br />

## Correlation of Numeric Features
<p align="center">
  <img src="https://github.com/user-attachments/assets/0b36c490-09a2-4580-9ef6-3c05a04eeb66" height="80%" width="80%" alt="Correlation Matrix"/>
</p>
<p>

- Analysis:
  
    - Generate a correlation matrix to identify any multicollinearity between numerical features.
  
    - In this dataset, no significant correlations were found that could adversely affect the classification models.

</p>
<br />

## Type of Drug Across Age
<p align="center">
  <img src="https://github.com/user-attachments/assets/5ee20395-4b3d-47b5-8e6d-7ba2c0818ccb" height="80%" width="80%" alt="Drug and Age"/>
</p>
<p>

- Insights:

  - Analyze the relationship between patients' age and the type of drug administered.

  - Observation: Drug B is predominantly prescribed to an older demographic.

</p>
<br />

## Type of Drug Across Sodium Level
<p align="center">
  <img src="https://github.com/user-attachments/assets/8903c408-ef74-447a-b49b-ecc04563a78d" height="80%" width="80%" alt="Drug and Sodium"/>
</p>
<p>

- Insights:

   - Examine how different drugs correlate with patients' sodium levels.
     
   - Observation: All drug types are administered within a normal sodium level distribution range, indicating no significant variation.

</p>
<br />

## Type of Drug Across Potassium Level
<p align="center">
  <img src="https://github.com/user-attachments/assets/4105f5cd-e2b9-4c39-aba2-c33f8ef6930d" height="80%" width="80%" alt="Drug and Potassium"/>
</p>
<p>

- Insights:

  - Investigate the relationship between potassium levels and drug types.
  
  - Observation: Drug Y is predominantly administered to patients with lower potassium levels.

</p>
<br />

# Feature Engineering the Data

## Label Encoding Categorical Variables
<p align="center">
  <img src="https://github.com/user-attachments/assets/d1e4d9aa-3869-4baf-adf8-93a5191dad25" height="80%" width="80%" alt="Recode into Different Variables"/>
</p>
<p>

- Process:

  - Convert categorical variables into numerical format using label encoding.

  - Assign numerical labels to each category without implying any ordinal relationship, as the categories are nominal.
  
</p>
<br />

## Scaling Numeric Values
<p align="center">
  <img src="https://github.com/user-attachments/assets/b92a3ba4-2e5b-4f28-a1a0-21cd46ca2b90" height="80%" width="80%" alt="Scale Numerics"/>
</p>
<p>

- Process:

  - Apply Z-score normalization to standardize numerical features.

  - This scaling technique centers the data around the mean with a standard deviation of one, facilitating better performance for certain classification algorithms.

</p>
<br />

# Classification Models

## K Nearest Neighbors (85% Accuracy)
<p align="center">
  <img src="https://github.com/user-attachments/assets/9a2222c6-8533-48e2-b6f2-112af49ae177" height="80%" width="80%" alt="SPSS KNN Output"/>
</p>
<p>

- Performance:

  - Achieved an accuracy of 85% using a 70/30 train-test split with K=5.

- Model Explanation:

  - The K-Nearest Neighbors (KNN) algorithm classifies a data point based on the majority label of its 'K' closest neighbors in the feature space.
  
  - In this case, for each unknown drug, the algorithm identifies the five nearest data points and assigns the drug type that is most common among them.
  
</p>
<br />

## Multinomial Logistic Regression Model (100%)
<p align="center">
  <img src="https://github.com/user-attachments/assets/f1ef1e18-142e-421c-8068-e6e5e471187e" height="60%" width="60%" alt="SPSS MN LR Output"/>
</p>
<p>
  
- Performance:

  - Achieved a perfect accuracy of 100% on the training data.

- Analysis:

  - While the Multinomial Logistic Regression model performed exceptionally well, there is a potential risk of overfitting.

  - Comparable studies by other data scientists have reported accuracies around 97.5%, suggesting that the model may need regularization or validation on a separate dataset to ensure generalizability.

</p>
<br />

## Decision Tree (70%)
<p align="center">
  <img src="https://github.com/user-attachments/assets/e904aa38-5094-4e63-bd39-29e9ac45f0d9" height="80%" width="80%" alt="SPSS DT Output"/>
</p>
<p>

- Performance:

  - Achieved an accuracy of 70%.

- Analysis:

  - The Decision Tree model showed relatively lower accuracy compared to KNN and Logistic Regression.

  - This may be due to overfitting, insufficient depth, or the inherent nature of the dataset not aligning well with tree-based methods.
  
</p>
<br />

# Conclusion

This project successfully classified unknown cardiovascular drugs using IBM SPSS Statistics with varying degrees of accuracy across different models. The Multinomial Logistic Regression model demonstrated the highest accuracy, albeit with potential overfitting concerns. K-Nearest Neighbors also performed commendably, providing a balanced approach between simplicity and effectiveness. The Decision Tree model, while less accurate, offers interpretability that could be valuable for understanding feature importance.

# Next Steps
Model Validation:
  
  - Implement cross-validation techniques to assess the generalizability of the models, particularly the Multinomial Logistic Regression.

Hyperparameter Tuning:
  
  - Optimize model parameters (e.g., the value of 'K' in KNN) to enhance performance.

Feature Selection:
  
  - Explore feature importance and reduce dimensionality to improve model efficiency and accuracy.

Handling Imbalanced Data:
  
  - If applicable, apply techniques such as SMOTE to address any class imbalances in the dataset.

Deployment:
  
  - Develop a user-friendly interface or integrate the model into a healthcare application for real-time drug classification.

Extended Analysis:
  
  - Incorporate additional datasets or variables to enrich the analysis and improve classification robustness.

## References

- [IBM SPSS Statistics Documentation](https://www.ibm.com/support/pages/ibm-spss-statistics-28-documentation)

- [Kaggle Cardiovascular Dataset](https://www.kaggle.com/code/matinmahmoudi/drug-classification-quick-start-for-beginners/input)

- Relevant literature on classification algorithms and their applications in healthcare.

## Contact
For any queries or further discussion, please contact Julian Sotelo at [jasotel1@outlook.com].

## License
This project is licensed under the MIT License.

## Acknowledgments
Thanks to the contributors of the Kaggle dataset.
Appreciation to the IBM SPSS community for their extensive resources and support.
