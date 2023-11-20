# Credit-Card-Fraud-Detection-System

Project for:-
School of Computer Science
KIIT
Course: Computer Networks (IT-3009)
Project Topic: Credit Card Fraud Detection System


Project Overview
Introduction
This project aims to demonstrate a typical end-to-end machine learning pipeline for credit card fraud detection. The current file provides an overview of the problem context, data requirements, modeling techniques, and performance evaluation involved in developing robust fraud detection systems. The next steps will focus on more rigorous validation before real-world deployment.

Project Objectives

Understanding Credit Card Fraud - 
Credit card fraud encompasses a variety of deceptive activities aimed at exploiting the financial systems associated with credit cards. The types of credit card fraud are diverse, ranging from identity theft to account takeover and skimming. Identity theft involves stealing personal information to open fraudulent credit card accounts, while account takeover occurs when criminals gain unauthorized access to existing accounts. Skimming involves the use of devices to capture credit card information during legitimate transactions.


Exploring Data Sources for credit card transaction information involves a comprehensive approach to identify and acquire datasets that encompass both legitimate and fraudulent transactions. The selection process should prioritize datasets that reflect real-world scenarios, ensuring a balanced representation of normal and anomalous activities. It is crucial to obtain diverse datasets from various sources, such as financial institutions, e-commerce platforms, and other relevant industries, to capture the complexity and variability of credit card transactions. The quality of the datasets is paramount, with a focus on accuracy, completeness, and relevance to the task at hand.


Data Preprocessing is a crucial phase in the data analysis and modeling pipeline, involving the systematic cleaning and transformation of acquired data to enhance its quality and suitability for further analysis. This multifaceted process encompasses the identification and elimination of noise and inconsistencies within the dataset, ensuring that the information used for analysis is accurate and reliable. Additionally, data is transformed into a standardized and appropriate format, facilitating ease of interpretation and analysis. Handling missing values is another critical aspect of preprocessing, as it involves deciding whether to impute or remove incomplete data points, thereby preserving the integrity of the dataset. Furthermore, outlier detection and treatment are vital to prevent skewed results and ensure that statistical models are not unduly influenced by extreme values. Overall, meticulous data preprocessing lays the foundation for robust and meaningful analyses, enhancing the accuracy and reliability of subsequent modeling endeavors.


Feature extraction is a critical step in developing an effective fraud detection model, especially when working with transaction data. In this process, the goal is to identify and investigate relevant features that can serve as input to the model. These features could include transaction amount, frequency, time of day, location, and any other pertinent information. Once potential features are identified, it is essential to assess their significance in distinguishing between legitimate and fraudulent transactions. Statistical methods, correlation analysis, and domain expertise can aid in understanding the impact of each feature on the model's ability to identify fraud. Feature optimization becomes crucial in enhancing model performance, as selecting the most relevant features helps prevent overfitting and improves the model's generalizability. By iteratively refining the feature set, the fraud detection model can achieve better accuracy and robustness in identifying suspicious activities within transaction data.


ML Algorithm Selection & Model Design - 
This study explores the application of Random Forest algorithms for fraud detection in credit card transactions. Utilizing the 'undersampled_data.csv' dataset, the study ensures balanced class representation before preprocessing the data. Preprocessing involves converting the 'Amount' column to float values, encoding categorical columns using LabelEncoder, and splitting the data into training and test sets. A RandomForestClassifier model is trained on the training data and evaluated on the test data, achieving over 90% accuracy. The study also demonstrates the model's capability to make predictions on new data points and saves the trained model for future use.

 1. Import necessary libraries like pandas and imblearn.under_sampling
 2. Load the original imbalanced dataset into a pandas DataFrame
 3. Separate the independent (or feature) columns from the dependent (or target) column
 4. Create an instance of RandomUnderSampler from imblearn and fit it on the independent and dependent data
 5. This will balance the data by randomly selecting samples from the majority class to match the number of samples in the minority class
 6. Convert the undersampled data back into a DataFrame with the original columns
 7. Add the target variable as a new column in this DataFrame
 8. Save the balanced DataFrame to a new CSV file

The key steps are using RandomUnderSampler to undersample the majority class and then saving the balanced data to a new file that can be used for model training. This allows you to balance the original imbalanced dataset to have equal samples of each class.

Validation and Testing
  - Data preprocessing steps include:
      - Converting amount to float by removing currency symbols
      - Encoding categorical features like UseChip, MerchantName etc using LabelEncoder
  - A Random Forest Classifier model is built with 100 estimators and entropy criterion.
  - The data is split into training (2/3rd) and test sets (1/3rd) for modeling.
  - Model achieves ~92% accuracy on test data with high precision and recall scores, indicating good performance.
  - Cross-validation is not explicitly done but train-test split provides a way to assess generalization capability.

Conclusion
This project focuses on developing a machine learning model for credit card fraud detection. The text emphasizes the importance of understanding fraud patterns, acquiring diverse datasets, thorough data preprocessing, and careful feature engineering. A Random Forest algorithm is applied to an undersampled credit card transaction dataset, achieving over 90% accuracy on the test set. However, further validation through cross-validation and hyperparameter tuning is recommended. The project exemplifies a typical machine learning workflow for credit card fraud detection, demonstrating the need for rigorous validation and testing before real-world deployment.
