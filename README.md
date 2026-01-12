# Swiggy-Restaurant-Performance-Pricing-Analysis
This project analyzes restaurant-level data from an online food delivery platform (Swiggy) to derive insights on pricing, customer ratings, cuisine distribution and delivery operations.

# Dataset
- <a href="https://github.com/ankkona/Swiggy-Restaurant-Performance-Pricing-Analysis/blob/main/Swiggy%20Dataset.xlsx">Swiggy Restaurant Data</a>

# Data Cleaning
- **Ratings**
     - Created an additional column **Ratings_Range** to capture the numeric rating ranges corresponding to each rating label.
     - Converted raw numeric ratings into categorical labels **(Poor, Average, Good, Excellent)** to facilitate meaningful analysis.
- **Food Category**: Cleaned and consolidated food type data into a binary feature: **Veg / Non-Veg**.
- **Cost Validation**: Created a column to mark cost values as Valid or Invalid.
- **Cost Cleanup**: Identified invalid cost entries and removed outliers **(values below 100)** to maintain data integrity.
- **Budget Category**: Engineered a **Budget_Category** feature by segmenting cost into meaningful ranges: **Mid Range, Budget, Premium**.
- **Locality Cleanup**: Addressed missing locality information by replacing nulls in the Locality column with corresponding values from the Area column.
- **Long-Distance Delivery**: Created a derived binary feature **Distance_flag** to indicate delivery distance: **Long Distance / Normal**.

