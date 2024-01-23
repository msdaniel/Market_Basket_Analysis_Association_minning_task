# Market_Basket_Analysis_Association_minning_task

# Association Rules Mining: Market Basket Analysis on an Online Retail Dataset

## 1. Introduction

Market Basket Analysis is an association rule mining technique that explores customers' shopping behavior by identifying associations between items placed in their shopping baskets. This project employs Association Rule Mining, a rule-based machine learning method, to uncover meaningful correlations between different products based on their co-occurrence in a dataset.

### 1.1 Motivation

Market Basket Analysis helps uncover insights into customer buying habits, providing valuable knowledge for retailers to enhance their marketing strategies and optimize product placements.

### 1.2 Methodology

The analysis in this report focuses on using Association Rule Mining to answer the question: If a customer buys a certain product, is it necessary that the customer will buy another product related to that purchase?

## 2. Datasets

The project utilizes an online retail dataset publicly available on the [UCI Machine Learning Repository] https://archive.ics.uci.edu/dataset/352/online+retail . The dataset is a transnational data set containing all transactions occurring between 01/12/2010 and 09/12/2011 for a UK-based and registered non-store online retail.

### 2.1 Data Preprocessing

- The dataset is an Excel document with 541,909 rows and 8 columns.
- Missing values in 'Description' (1454 records) and 'CustomerID' (135,080 records) were dropped as they constitute less than 1% of the total data.
- Duplicated rows (5225 records) were removed while keeping the first transactional observation.
- Cancelled transactions were identified based on the 'InvoiceNo' column (starting with the letter 'C') and removed.
- Additional columns 'Year', 'Month', and 'Day' were created by extracting values from the 'InvoiceDate' column.
- The 'Description' column was stripped to remove white spaces, and the 'InvoiceNo' column was changed to the string data type.
- The analysis focuses on records from the United Kingdom, which constitutes 91% of the dataset.

### 2.2 Data Exploration

Exploratory data analysis (EDA) was performed on the preprocessed data to gain insights into customer transaction patterns and identify potential associations between products.

## 3. Implementation

The market basket analysis in this report was performed using  the Apriori algorithm. The code and detailed analysis can be found in the corresponding code file.

### 3.1 Dependencies

Ensure you have the following dependencies installed before running the code:

- Python 3.8+
- Pandas
