# Outfit-Recommendations-with-Instant-Google-Search

This code implements a product recommendation system for luxury apparel using text analysis and similarity matching. Here's a detailed summary of what the code does:
1. Data Import and Initial Processing:
   - Imports necessary libraries: numpy, pandas, matplotlib, seaborn
   - Loads a CSV file named 'Luxury_Products_Apparel_Data.csv' into a pandas DataFrame
   - Performs basic data cleaning: removes null values and renames the 'Unnamed: 0' column to 'ID'
2. Exploratory Data Analysis:
   - Generates frequency plots for 'Category' and 'SubCategory' columns
   - Calculates and displays the percentage of unique ProductNames and Descriptions
   - Creates histograms for the length of Description and ProductName fields
3. Text Preprocessing:
   - Defines a 'preprocess' function that:
     - Converts text to lowercase
     - Expands contractions (e.g., "don't" to "do not")
   - Applies this preprocessing to the 'Description' column
4. TF-IDF Vectorization:
   - Uses sklearn's TfidfVectorizer to convert the preprocessed descriptions into TF-IDF vectors
   - This step quantifies the importance of words in the product descriptions
5. Similarity-based Recommendation System:
   - Implements a function 'get_top_similar_products' that:
     - Takes a new product description as input
     - Calculates cosine similarity between this input and all products in the dataset
     - Returns the top 5 most similar products
6. User Interface:
   - Prompts the user to enter a product description
   - Displays the top 5 similar products in an HTML table format
   - For each recommended product, it shows:
     - Category
     - Subcategory
     - Product Name
     - A Google Search link for the product
7. Visualization and Display:
   - Uses IPython's HTML display capabilities to show results in a formatted table
   - Includes hyperlinks to Google searches for each recommended product
This code essentially creates a system where a user can input a description of a luxury apparel item, and the system will return the top 5 most similar products from its database, based on the textual similarity of the descriptions. It combines techniques from data preprocessing, text analysis (TF-IDF), and similarity measures (cosine similarity) to achieve this recommendation functionality.
