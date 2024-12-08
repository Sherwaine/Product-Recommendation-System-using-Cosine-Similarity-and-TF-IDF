# Product Recommendation System using Cosine Similarity and TF-IDF

This repository contains the implementation of a product recommendation system based on the cosine similarity between product descriptions using the **TF-IDF** (Term Frequency-Inverse Document Frequency) technique. This system is designed to recommend products that are similar to a given product description.

## Overview

This recommendation system processes product descriptions and calculates the similarity between them using cosine similarity. The system then suggests the top 5 products that are most similar to a provided input product description. The cosine similarity measures the closeness between products based on the textual content of their descriptions.

## Key Features
- **Cosine Similarity**: A metric to measure the similarity between two vectors (in this case, the TF-IDF vectors of product descriptions).
- **TF-IDF Vectorization**: Converts product descriptions into numerical vectors based on word frequency, while down-weighting common words and emphasizing rare ones.
- **Recommendations**: Provides the top 5 most similar products, excluding the input product itself.

## Requirements

Before running the script, ensure you have the following dependencies installed:

- Python 3.x
- Pandas
- Scikit-learn
- OpenPyXL (for reading Excel files)

You can install the required Python libraries using `pip`:

```bash
pip install pandas scikit-learn openpyxl


Usage
Step 1: Prepare Your Dataset
The system works on a dataset with at least one column containing product descriptions. In this example, the dataset is assumed to be in an Excel file named Online Retail.xlsx. The column containing the product descriptions should be named Description.

Make sure to update the path of the dataset in the code if necessary.

Step 2: Run the Code
The script will read the dataset and perform the following steps:

Preprocess the data by converting all descriptions to strings and handling missing values.
Vectorize the product descriptions using TF-IDF.
Calculate the cosine similarity between the descriptions.
Provide product recommendations based on the input description.

Step 3: Customize the Input
To get recommendations for any other product, simply change the product_description variable to any valid product description from your dataset. The function get_recommendations will return the top 5 most similar products.

Functions
get_recommendations(product_description, cosine_sim_matrix, df)
Input:
product_description (str): The description of the product for which you want recommendations.
cosine_sim_matrix (numpy array): The precomputed cosine similarity matrix for product descriptions.
df (DataFrame): The pandas DataFrame containing the product data (with a column Description).
Output:
Returns a list of the top 5 most similar products along with their similarity scores.
Example Dataset
For the recommendation system to work, the dataset should have at least the following columns:

Description: Contains the textual descriptions of the products.
Sample Data (first few rows):
Description	Price	Quantity
WHITE HANGING HEART T-LIGHT HOLDER	2.99	50
VINTAGE T-LIGHT HOLDER	3.50	30
HANGING T-LIGHT HOLDER WITH HEART	4.00	25
CERAMIC T-LIGHT HOLDER	5.00	10
SILVER T-LIGHT HOLDER	3.75	15
Ensure your dataset is clean, with descriptions being string type and free from excessive missing values for the best results.