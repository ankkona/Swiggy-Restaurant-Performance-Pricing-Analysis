# Swiggy-Restaurant-Performance-Pricing-Analysis
This project analyzes restaurant-level data from an online food delivery platform (Swiggy) to uncover insights into pricing strategy, customer ratings, cuisine preferences, and city-level performance.

# Dataset
The dataset contains restaurant-level information including ratings, cost, cuisine, city, food type, and delivery distance.
- <a href="https://github.com/ankkona/Swiggy-Restaurant-Performance-Pricing-Analysis/blob/main/Swiggy%20Dataset.xlsx">Swiggy Restaurant Data</a>

# Tech Stack
- Microsoft Excel
- Pivot Tables & Pivot Charts
- Advanced Excel Charts (Bar, Column, Stacked Bar, Donut, Scatter Plot)
- Data Cleaning & Validation
- Calculated Fields & Derived Metrics
- KPI Design
- Interactive Dashboards using Slicers

# Dashboard
<img src="https://github.com/ankkona/Swiggy-Restaurant-Performance-Pricing-Analysis/blob/main/1.png" alt="Dashboard Demo" width="1200"/>

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
- __Restaurant Ratings Distribution__
   - Most restaurants fall in the 3.5–4.5 rating range (78% of restaurants), showing generally good quality.
   - Very few (<3%) are below 3.0, indicating minimal poor-performing restaurants.

- __Impact of Pricing on Ratings__
   - Premium restaurants consistently have higher average ratings (~4.0–4.2).
   - Mid-range restaurants dominate the market with moderate ratings (~3.9–4.1).
   - Budget restaurants have the highest quantity but slightly lower ratings (~3.8–4.0).

- __City Performance (Quality + Scale)__
  - Kolkata: Highest weighted score → strong market impact due to both high rating and high restaurant count.
  - Mumbai: Highest average rating but fewer restaurants → high quality, smaller scale.
  - Ahmedabad: High count but lower average rating → potential quality risk.
  - Indore, Nagpur: Low rating + low count → low priority for expansion.

- __Veg vs Non-Veg Distribution__
   - Non-Veg restaurants dominate (~72%), Veg options are only ~28%.
   - There is opportunity to expand vegetarian offerings in markets with high non-veg concentration.

- __Cuisine Popularity & Ratings__
  - Most popular cuisines by count: North Indian, Chinese, Indian, Fast Food.
  - High-rating niches: Bakery, Desserts maintain strong ratings despite lower counts → opportunity to grow specialty segments.

- __Premium Restaurant Performance__
  - Premium restaurants consistently outperform in ratings (~4.0–4.2), indicating better customer satisfaction.
  - Mid-range and budget restaurants show mixed performance.

- __City Quadrant Insights__
  - High Rating + High Count: Kolkata, Pune → strong, mature markets
  - High Rating + Low Count: Mumbai → expansion opportunity
  - Low Rating + High Count: Ahmedabad → quality risk
  - Low Rating + Low Count: Indore, Nagpur → low priority

# What should the organisation do next?
- Expand selectively in high-rating, low-count cities (e.g., Mumbai) by onboarding more quality restaurants to scale strong customer satisfaction without diluting quality.
- Address quality gaps in low-rating, high-count cities (e.g., Ahmedabad) through partner audits, menu standardization, and rating-linked incentive programs.
- Prioritize promotion of premium and mid-range restaurants, as these segments consistently demonstrate higher average customer ratings.
- Leverage high-rated but underrepresented cuisines (e.g., desserts, bakery) for targeted campaigns to diversify demand and increase repeat orders.
- Support budget restaurants with quality improvement initiatives (pricing transparency, packaging standards, menu optimization) to lift overall platform ratings.
- Use the city performance quadrant (rating vs. count) as a recurring decision framework for market expansion, retention, and operational focus.
  
# Expected Impact
- Higher customer satisfaction and retention by systematically addressing low-rating segments and cities.
- Revenue and order value uplift through increased visibility and adoption of premium and high-rated restaurants.
- Reduced operational risk by prioritizing expansion in proven high-quality markets.
- More efficient marketing spend by focusing on high-impact cuisines and city segments rather than broad promotions.
- Sustainable platform growth driven by data-backed city and category prioritization.

# Assumptions & Limitations
- Customer ratings are assumed to reasonably reflect satisfaction, though they may be influenced by subjectivity or varying review volumes across restaurants.
- Pricing data (cost for two) is treated as static and does not account for discounts, surge pricing, or time-based offers.
- The analysis excludes operational metrics such as delivery time, order cancellations, and partner availability, which may also affect customer experience.


