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
- The overall average rating is 3.9, indicating generally positive but improvable customer satisfaction.
- Only 23.2% of restaurants fall into the high-rated category, highlighting a quality improvement opportunity.
- Restaurants with higher cost ranges (>600) achieve the highest average ratings (≈4.16), suggesting a strong pricing–quality relationship.
- Non-Veg restaurants dominate the platform (72.5%), reflecting customer demand patterns.
- Kolkata emerges as the best performing city when combining rating and restaurant count (weighted impact).
- The City Performance Matrix shows:
    - Kolkata and Pune as strong, mature markets (high rating + high count).
    - Mumbai as high rating but moderate count, indicating expansion potential.
    - Cities like Indore and Nagpur fall into low rating + low count, making them lower priority.
- Certain cuisines (e.g., Desserts, Beverages) show high ratings despite lower volumes, indicating niche strengths.

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
# What should the organisation do next best on your findings?
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


