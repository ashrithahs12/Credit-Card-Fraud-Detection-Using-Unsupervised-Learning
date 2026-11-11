# Credit Card Fraud Detection Using Unsupervised Learning

## Project Overview

Credit card fraud detection is an important application of Machine Learning in the financial industry. Fraudulent transactions are rare compared to legitimate transactions, making them difficult to identify.

This project uses **Unsupervised Learning techniques** to identify unusual patterns in credit card transactions and detect potentially fraudulent activities.

Two algorithms, **K-Means Clustering** and **Isolation Forest**, are implemented and compared to determine which method is more effective in identifying suspicious transactions.

## Objectives

- Analyze credit card transaction data using Exploratory Data Analysis (EDA).
- Identify unusual transaction patterns without using fraud labels during model training.
- Apply K-Means Clustering for identifying transactions that are far from cluster centers.
- Apply Isolation Forest for detecting anomalous transactions.
- Compare both models using Precision, Recall, and Confusion Matrix.
- Identify the more suitable model for fraud detection.

## Technologies Used

- **Programming Language:** Python
- **Environment:** Jupyter Notebook / Google Colab
- **Libraries:**
  - Pandas – Data manipulation and analysis
  - NumPy – Numerical operations
  - Matplotlib – Data visualization
  - Seaborn – Statistical visualization
  - Scikit-learn – Machine Learning algorithms and evaluation

## Dataset Description

The project uses a credit card transaction dataset containing:

- **Total Transactions:** 284,807
- **Total Features:** 31
- **Legitimate Transactions:** 284,315
- **Fraudulent Transactions:** 492
- **Fraud Percentage:** 0.1727%

The dataset contains the following features:

- `Time` – Time elapsed between transactions.
- `V1` to `V28` – PCA-transformed transaction features.
- `Amount` – Transaction amount.
- `Class` – Actual transaction label (0 = Legitimate, 1 = Fraudulent).

**Note:** The `Class` column is excluded during model training and used only for final evaluation.

## Project Workflow

### 1. Problem Understanding
Understanding credit card fraud detection and the importance of unsupervised learning when fraud labels are unavailable or delayed.

### 2. Exploratory Data Analysis (EDA)
- Understanding dataset dimensions and features.
- Analyzing numerical feature distributions.
- Visualizing transaction amounts.
- Identifying class imbalance.
- Extracting important statistical insights.

### 3. Data Preprocessing
- Separating transaction features and actual labels.
- Excluding the `Class` column from model training.
- Applying StandardScaler for feature scaling.

### 4. K-Means Clustering
- Applying K-Means clustering to group similar transactions.
- Selecting the number of clusters using the Silhouette Score.
- Calculating distances from cluster centers.
- Identifying transactions exceeding the anomaly threshold.

### 5. Isolation Forest
- Applying Isolation Forest for anomaly detection.
- Identifying unusual transaction patterns.
- Separating normal and anomalous transactions.

### 6. Model Comparison
Comparing K-Means and Isolation Forest based on their anomaly detection results and advantages and limitations.

### 7. Bonus Evaluation
- Comparing model predictions with actual fraud labels.
- Generating confusion matrices.
- Calculating Precision and Recall.
- Selecting the more suitable model.

## Model Performance and Results

The following results were obtained during model evaluation:

| Evaluation Metric | K-Means | Isolation Forest |
|---|---:|---:|
| Precision | 10.42% | 4.07% |
| Recall | 60.37% | 81.91% |
| Actual Fraud Detected | 297 | 403 |

### Key Findings

- K-Means identified 2,849 anomalous transactions.
- Isolation Forest identified 9,895 anomalous transactions.
- K-Means achieved higher precision.
- Isolation Forest achieved higher recall.
- Isolation Forest detected more actual fraudulent transactions and missed fewer fraud cases.

## Conclusion

This project demonstrates how unsupervised learning techniques can be used to identify potentially fraudulent credit card transactions without using actual fraud labels during model training.

Among the two algorithms, **Isolation Forest was selected as the more suitable model** because it achieved a higher recall of 81.91%, compared to 60.37% for K-Means.

Although Isolation Forest produces more false positives, it identifies more actual fraudulent transactions. Therefore, it can be used as an initial fraud screening approach, with further investigation required before confirming suspicious transactions as fraud.


## Future Improvements

- Improve model precision and reduce false positives.
- Experiment with additional anomaly detection techniques.
- Optimize model parameters for better detection performance.
- Develop a real-time fraud monitoring application.

## Author

**H S Ashritha**

**Project Type:** Minor Project 4

**Domain:** Machine Learning | Unsupervised Learning | Fraud Detection
