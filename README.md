# Swiggy-Restaurant-Performance-Pricing-Analysis
This project analyzes restaurant-level data from an online food delivery platform (Swiggy) to uncover insights into pricing strategy, customer ratings, cuisine preferences, and city-level performance. This analysis identifies how pricing tiers, city scale, and cuisine mix influence customer satisfaction on Swiggy. Using a quality-vs-scale framework, the project highlights where Swiggy should expand, where quality must be fixed before scaling, and which segments offer the highest return on investment.
 
# Dataset
The dataset contains restaurant-level information including ratings, cost, cuisine, city, food type, and delivery distance.This analysis uses a publicly available dataset for educational and portfolio purposes.
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
<img src="https://github.com/ankkona/Swiggy-Restaurant-Performance-Pricing-Analysis/blob/main/Dashboard.png" width="1200"/>

# Data Cleaning
- **Primary Cuisine** : Extracted the first cuisine listed from the original cuisine column.
- **Primary Cuisine Cleaned** : Consolidated similar categories by merging Sweets and Ice Creams into a single Desserts category.
- **Ratings**
     - Created an additional column **Ratings_Range** to capture the numeric rating ranges corresponding to each rating label.
     - Converted raw numeric ratings into categorical labels **(Poor, Average, Good, Excellent)** to facilitate meaningful analysis.
- **Cost Validation**: Created a column to mark cost values as Valid or Invalid.
- **Cost Cleanup**: Identified invalid cost entries and removed outliers **(values below 100)** to maintain data integrity.
- **Cost Range** : Bucketed cost values into defined ranges: ≤200, 200–400, 400–600, >600.
- **Budget Category**: Engineered a **Budget_Category** feature by segmenting cost into meaningful ranges: **Mid Range, Budget, Premium**.
- **Food Category**: Cleaned and consolidated food type data into a binary feature: **Veg / Non-Veg**.
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
   - The majority of restaurants (~78%) fall within the 3.5–4.5 rating range, indicating generally good and consistent quality across the platform.
   - A small proportion (3.5%) of restaurants are rated below 3.0, suggesting limited presence of poorly performing outlets.

- __Impact of Pricing on Ratings__
   - Budget restaurants form the largest share of the platform, which is why they contribute the highest absolute number of restaurants across all rating bands. However, they also show a wider spread into lower rating categories (<3.5), indicating greater variability in customer experience.
   - Mid-range restaurants are more concentrated in the 3.5–4.5 rating bands, suggesting relatively stable and predictable quality, though with limited presence in the highest (4.5+) tier.
   - Premium restaurants, despite being fewer in number, show a strong concentration in higher rating ranges (4.0+) and minimal presence in low-rating bands, indicating more consistent customer satisfaction rather than higher volume.

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
  - __High Rating + High Restaurant Count (Strong & Mature Markets) - Kolkata, Pune__
    - These cities perform well on both customer satisfaction and scale. They are established markets delivering consistent quality with a large number of restaurants.
  - __High Rating + Low Restaurant Count (High Potential for Expansion) - Mumbai, Ahmedabad__
    - Both cities show strong average ratings but have relatively fewer restaurants. This indicates good customer experience with room to expand supply without hurting quality.
  - __Low Rating + High Restaurant Count (Quality Improvement Needed) - Ghaziabad, Delhi__
    - These markets have many restaurants but sit below the average rating line, suggesting operational or quality consistency issues that should be addressed before further expansion.
  - __Low Rating + Low Restaurant Count (Low Priority Markets)- Lucknow, Hyderabad, Indore, Nagpur__
    - These cities currently show weaker performance on both scale and ratings, making them lower priority for immediate growth or investment.

# What should the organisation do next?
- Protect and strengthen mature markets (Kolkata, Pune)
Focus on partner retention, operational efficiency, and premium visibility rather than aggressive expansion, since both scale and quality are already strong.
- Expand supply in Mumbai cautiously but deliberately
Mumbai shows excellent customer satisfaction but lower restaurant density; onboarding should prioritize quality-first partners to scale without eroding ratings.
- Fix quality before scaling in Delhi and Ghaziabad
These cities already have scale, so the priority should be rating improvement initiatives (partner audits, menu consistency, service standards) rather than adding more restaurants.
- Treat Ahmedabad, Lucknow, Hyderabad, Indore, and Nagpur as incubation markets
Expansion should be selective and data-driven, focusing on improving customer experience and identifying strong local performers before committing larger investments.
- Use the city performance matrix as a control mechanism
Any city should move right (scale) only after it moves up (quality), using rating benchmarks as a gate for expansion decisions.
  
# Expected Impact
- Higher customer satisfaction and retention by systematically addressing low-rating segments and cities.
- Revenue and order value uplift through increased visibility and adoption of premium and high-rated restaurants.
- Reduced operational risk by prioritizing expansion in proven high-quality markets.
- More efficient marketing spend by focusing on high-impact cuisines and city segments rather than broad promotions.
- Sustainable platform growth driven by data-backed city and category prioritization.

# Assumptions & Limitations
- Customer ratings are assumed to reasonably reflect satisfaction, though they may be influenced by subjectivity or varying review volumes across restaurants.
- Pricing data (cost for two) is treated as static and does not account for discounts, surge pricing, or time-based offers.
- Veg / Non-Veg classification is defined at the restaurant level rather than at the cuisine or item level, which may lead to unintuitive combinations (e.g., beverages or specific cuisines appearing as non-veg).
- The analysis excludes operational metrics such as delivery time, order cancellations, and partner availability, which may also affect customer experience.


