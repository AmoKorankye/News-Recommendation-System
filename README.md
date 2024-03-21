## News Recommendation System using Cosine Similarity

This Python code aims to build a news recommendation system based on the content similarity between news articles' titles. Here's a breakdown of what the code accomplishes:

### 1. Data Loading and Exploration
- The code starts by importing necessary libraries including numpy, pandas, matplotlib, and scikit-learn modules.
- It reads a dataset called 'News.csv' using Pandas `read_csv` function.
- The first few rows of the dataset are displayed using `head()` function to understand its structure.

### 2. Data Visualization
- It calculates the distribution of news categories and stores the counts in the `categories` variable.
- Then, it extracts labels and counts for each category.
- The distribution of news categories is visualized using a bar plot created with Matplotlib.

### 3. Text Processing and Feature Extraction
- The titles of news articles are extracted from the dataset and stored in the `feature` variable.
- The TF-IDF vectorizer is used to convert the text data into numerical vectors.
- Stop words (commonly occurring words like 'the', 'is', etc.) are removed during vectorization.
- TF-IDF matrix is generated using `fit_transform()` function from scikit-learn.

### 4. Similarity Computation
- Cosine similarity is calculated between TF-IDF vectors of news titles.
- The resulting similarity matrix represents how similar each pair of news articles is based on their titles.

### 5. Recommendation Function
- A function named `news_recommendation` is defined to recommend news articles similar to a given news title.
- It takes a news title as input and returns the top 10 most similar news titles based on cosine similarity.
- Inside the function, it retrieves the index of the input news title from the indices series.
- Then, it calculates similarity scores between the input title and all other titles.
- The similarity scores are sorted in descending order and the top 10 similar news indices are selected.
- Finally, it returns the titles corresponding to these similar indices.

### 6. Example Recommendation
- An example recommendation is made by calling `news_recommendation` function with a specific news title: "Walmart Slashes Prices on Last-Generation iPads".
- It prints out the top 10 recommended news titles that are most similar to the input title.

### Conclusion
This code implements a simple news recommendation system using cosine similarity based on the titles of news articles. It demonstrates how to preprocess text data, compute similarity scores, and recommend similar news articles based on user input.
