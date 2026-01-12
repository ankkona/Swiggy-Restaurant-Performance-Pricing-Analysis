# Swiggy-Restaurant-Performance-Pricing-Analysis
This project analyzes restaurant-level data from an online food delivery platform (Swiggy) to derive insights on pricing, customer ratings, cuisine distribution and delivery operations.

# Dataset
- <a href="https://github.com/ankkona/Swiggy-Restaurant-Performance-Pricing-Analysis/blob/main/Swiggy%20Dataset.xlsx">Swiggy Restaurant Data</a>
# Dashboard

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

# Business Questions
- How are restaurant ratings distributed across the platform?
- Does pricing (cost range / budget category) influence average customer ratings?
- Which cities perform best when considering both quality (rating) and scale (number of restaurants)?
- What is the proportion of Veg vs Non-Veg restaurants on the platform?
- Which cuisines are most popular, and how do their popularity and ratings compare?
- Are premium restaurants consistently delivering better customer satisfaction?
- Which cities represent growth opportunities versus quality risks?
  
# Key Insights
- Restaurant Ratings Distribution
   - Most restaurants fall in the 3.5–4.5 rating range (78% of restaurants), showing generally good quality.
   - Very few (<3%) are below 3.0, indicating minimal poor-performing restaurants.

- Impact of Pricing on Ratings
   - Premium restaurants consistently have higher average ratings (~4.0–4.2).
   - Mid-range restaurants dominate the market with moderate ratings (~3.9–4.1).
   - Budget restaurants have the highest quantity but slightly lower ratings (~3.8–4.0).

- City Performance (Quality + Scale)
  - Kolkata: Highest weighted score → strong market impact due to both high rating and high restaurant count.
  - Mumbai: Highest average rating but fewer restaurants → high quality, smaller scale.
  - Ahmedabad: High count but lower average rating → potential quality risk.
  - Indore, Nagpur: Low rating + low count → low priority for expansion.

- Veg vs Non-Veg Distribution
   - Non-Veg restaurants dominate (~72%), Veg options are only ~28%.
   - There is opportunity to expand vegetarian offerings in markets with high non-veg concentration.

- Cuisine Popularity & Ratings
  - Most popular cuisines by count: North Indian, Chinese, Indian, Fast Food.
  - High-rating niches: Bakery, Desserts maintain strong ratings despite lower counts → opportunity to grow specialty segments.

- Premium Restaurant Performance
 - Premium restaurants consistently outperform in ratings (~4.0–4.2), indicating better customer satisfaction.
 - Mid-range and budget restaurants show mixed performance.

- City Quadrant Insights
 - High Rating + High Count: Kolkata, Pune → strong, mature markets
 - High Rating + Low Count: Mumbai → expansion opportunity
 - Low Rating + High Count: Ahmedabad → quality risk
 - Low Rating + Low Count: Indore, Nagpur → low priority

# Dashboard
<img src="https://github.com/ankkona/Swiggy-Restaurant-Performance-Pricing-Analysis/blob/main/Dashboard.png" alt="Dashboard Demo" width="1000"/>

# Data Visuals
KPI Cards: Total Restaurants, Average Rating, % High-Rated Restaurants, Best Performing City.

Distribution of Restaurant Ratings: Shows concentration in the 3.5–4.5 range.

Average Rating by Cost Range: Demonstrates rating improvement with higher spend.

Veg vs Non-Veg Donut Chart: Highlights menu composition dominance.

Ratings by Budget Category (Stacked Bar): Compares quality distribution across Budget, Mid-Range, and Premium.

City Performance Matrix (Scatter Plot with Benchmarks): Strategic quadrant view of city performance.

Cuisine Ratings & Popularity (Combo Chart): Balances demand vs customer satisfaction.

# What should the organisation do next?
- Invest in high-rating, low-count cities (e.g., Mumbai) by onboarding more quality restaurants.
- Improve quality standards in low-rating but high-count cities through partner audits and incentives.
- Promote premium and mid-range restaurants, as they consistently outperform budget options in ratings.
- Use high-rated niche cuisines (e.g., desserts, beverages) for targeted marketing campaigns.
- Encourage budget restaurants to improve quality through pricing optimization and menu standardization.
- Leverage the city performance matrix to prioritize market expansion and operational focus.
  
# Expected Impact
- Improved customer satisfaction and retention by focusing on quality gaps.
- Higher order value and revenue uplift through premium restaurant promotion.
- Smarter city-level expansion decisions, reducing operational risk.
- More efficient marketing spend by targeting high-impact cuisines and cities.
- Long-term platform growth driven by data-backed strategic prioritization.


