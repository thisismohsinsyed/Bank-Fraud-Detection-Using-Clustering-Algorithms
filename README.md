# Bank Fraud Detection Using Clustering Techniques

This project focuses on using clustering techniques to detect fraudulent bank transactions. The aim is to identify anomalies in transaction data that might indicate fraudulent activity. This repository contains all the code, datasets, and resources required to replicate the results and gain insights into anomaly detection through clustering.

## Table of Contents
- [Introduction](#introduction)
- [Dataset Overview](#dataset-overview)
- [Features](#features)
- [Tech Stack](#tech-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Modeling Approach](#modeling-approach)
- [Evaluation](#evaluation)
- [Results](#results)
- [Future Work](#future-work)
- [Contributing](#contributing)
- [License](#license)

## Introduction
Bank fraud is a significant problem that affects both financial institutions and customers. In this project, we use clustering techniques to detect potentially fraudulent transactions without relying on labeled data. The goal is to group similar transactions into clusters and identify outliers, which are likely to be fraudulent activities.

## Dataset Overview
The dataset used for this project contains transaction data intended for analysis and fraud detection. It includes a range of attributes, such as transaction behavior, customer profiles, and contextual details that are critical for anomaly detection.

### Key Features of the Dataset:
- **TransactionID**: Unique identifier for each transaction.
- **AccountID**: Unique identifier for the account associated with the transaction.
- **TransactionAmount**: Monetary value of the transaction.
- **TransactionDate**: Date and time of the transaction.
- **TransactionType**: Categorical value ('Credit' or 'Debit').
- **Location**: Geographic location of the transaction.
- **DeviceID**: Unique identifier for the device used.

## Tech Stack
- **Python**: The core language used for this implementation.
- **Libraries**: `scikit-learn`, `pandas`, `numpy`, `matplotlib`, `seaborn`
- **Clustering Algorithms**: `K-Means`, `DBSCAN`, `Gaussian Mixture Models (GMM)`

## Installation
To get started, clone the repository and install the necessary dependencies:

```bash
# Clone the repository
git clone https://github.com/thisismohsinsyed/Bank-Fraud-Detection-Using-Clustering-Algorithms.git

# Change directory
cd Bank-Fraud-Detection-Using-Clustering-Algorithms

# Create a virtual environment
python -m venv venv

# Activate virtual environment (Windows)
venv\Scripts\activate

# Activate virtual environment (Linux/Mac)
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

## Usage
1. **Data Preprocessing**: Preprocess the dataset by cleaning missing values, normalizing numerical features, and creating new features.
2. **Training the Model**: Use clustering techniques like `K-Means`, `DBSCAN`, or `GMM` to identify clusters and potential fraudulent transactions.
3. **Running the API**: Start the Flask API for real-time fraud detection.

```bash
# Run the Flask API
python app.py
```

4. **Visualization**: Use the Streamlit dashboard to visualize cluster assignments and transaction details.

```bash
# Run the Streamlit app
streamlit run dashboard.py
```

## Modeling Approach
- **K-Means Clustering**: This method groups transactions into clusters, with the assumption that fraudulent transactions will fall into smaller, distinct clusters.
- **DBSCAN**: DBSCAN is used to detect outliers and define clusters of varying shapes and densities, which is useful for anomaly detection.
- **Gaussian Mixture Model (GMM)**: GMM is used to fit the data into different distribution components, identifying transactions that do not fit well into normal distributions.

## Evaluation
- **Silhouette Score**: Measures how similar transactions are to their own cluster compared to other clusters.
- **Davies-Bouldin Index**: Evaluates the compactness and separation between clusters.
- **Anomaly Detection Rate**: Measures the model's effectiveness in identifying anomalies.

## Results
- **DBSCAN** performed particularly well in identifying outliers, while **K-Means** effectively grouped normal transactions.
- Identified several small clusters of unusual transactions, likely to be fraudulent activities.

## Future Work
- **Real-Time Model Updates**: Implement a pipeline for real-time model updates with streaming data.
- **Graph-Based Features**: Add graph-based features to analyze relationships between accounts and transactions.

## Contributing
Contributions are welcome! If you have suggestions for improving the project, please fork the repository and submit a pull request.

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

If you find this repository helpful, please give it a star ⭐ and feel free to share your thoughts or suggestions.
