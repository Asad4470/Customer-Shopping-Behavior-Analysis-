<img width="1343" height="758" alt="Screenshot 2026-10-16 141915" src="https://github.com/user-attachments/assets/97da97d5-1258-4471-9d2c-43b6f62f77c6" />

Customer Shopping Behavior Analysis
An end-to-end data analytics portfolio project exploring retail customer shopping patterns using Python, PostgreSQL/SQL, and Power BI.

Project Overview
This project analyzes 3,900 purchase records across 18 columns to explore customer demographics, spending patterns, product preferences, discount behavior, shipping choices, review ratings, and subscription status.
The workflow combines data preparation in Python, business-focused SQL analysis in PostgreSQL, and an interactive Power BI dashboard. The goal is to turn transactional data into insights that can support retail decision-making.
Tools & Technologies
- Python: pandas, data cleaning, exploratory data analysis, feature engineering
- PostgreSQL / SQL: business queries, aggregations, ranking, customer segmentation
- Power BI: interactive dashboard, KPI cards, charts, and slicers
- GitHub: project documentation and portfolio versioning
Dataset Summary
Item	Details
Records	3,900 purchases
Columns	18
Missing values noted in source report	37 values in Review Rating
Main data areas	Customer demographics, purchase details, shopping behavior


Main fields
- Customer profile: Age, Gender, Location, Subscription Status
- Purchase details: Item Purchased, Category, Purchase Amount, Season, Size, Color
- Shopping behavior: Discount Applied, Promo Code Used, Previous Purchases, Frequency of Purchases, Review Rating, Shipping Type
Dataset note: Add the original dataset source and its license/usage terms here before publishing. Do not upload data you do not have permission to redistribute.

Workflow
1. Load and inspect data using pandas, df.info(), and df.describe().
2. Clean data by checking missing values and standardizing column names.
3. Handle missing ratings using the median review rating within each product category, as described in the project report.
4. Engineer features including age_group and purchase_frequency_days.
5. Check consistency between Discount Applied and Promo Code Used; the source report describes dropping Promo Code Used after checking redundancy.
6. Load cleaned data into PostgreSQL for SQL-based analysis.
7. Answer business questions with SQL queries.
8. Build a Power BI dashboard to communicate the analysis visually.
SQL Business Questions
The project investigates these questions:
1. How does total revenue compare by gender?
2. Which customers used discounts but spent above the average purchase amount?
3. Which five products have the highest average review ratings?
4. How do average purchase amounts compare between Standard and Express shipping?
5. How do average spending and total revenue compare for subscribers and non-subscribers?
6. Which five products have the highest share of discounted purchases?
7. How can customers be grouped into New, Returning, and Loyal segments based on purchase history?
8. What are the top three products within each category?
9. Are customers with more than five purchases more likely to subscribe?
10. Which age groups contribute the most revenue?
Dashboard
The Power BI dashboard includes:
- KPI cards for number of customers, average review rating, and average purchase amount
- Subscription-status breakdown
- Revenue by category
- Sales by category
- Sales by age group
- Revenue by age group
- Slicers for subscription status, gender, category, and shipping type
Example product-rating result
The supplied screenshot shows the following five items ranked by average product rating:
Item purchased	Average product rating
Gloves	3.86
Sandals	3.84
Boots	3.82
Hat	3.80
Skirt	3.78


These values are transcribed from the provided screenshot. Confirm the SQL query and aggregation before using them as a final business claim.
Business Recommendations
Based on the scope of the analysis, the project recommends investigating:
- Subscription growth: evaluate subscriber benefits and compare subscriber outcomes.
- Customer loyalty: reward repeat buyers and encourage returning customers.
- Discount strategy: assess discount effectiveness while considering profit margins, not revenue alone.
- Product promotion: feature well-rated and popular products, while checking review counts and sales volume.
- Targeted marketing: use age-group and shipping-pattern results to guide and test campaigns.
These are recommendations to validate against the final query results; they should not be presented as proven causal effects.
Repository Structure
customer-shopping-behavior-analysis/
├── README.md
├── LICENSE
├── notebooks/
│   └── customer_behavior_analysis.ipynb
├── sql/
│   └── business_analysis_queries.sql
├── powerbi_dashboard/
│   └── customer_behavior_dashboard.pbix
├── screenshots/
│   ├── customer-behavior-dashboard.png
│   └── top-rated-products.png
└── reports/
    └── Customer_Shopping_Behavior_Analysis_Professional_Report.pdf
Update the file names and folders to match the files you actually upload. Do not commit database passwords, API keys, or private connection strings.
Key Skills Demonstrated
- Data cleaning and missing-value treatment
- Exploratory data analysis and feature engineering
- PostgreSQL database integration
- SQL aggregation, ranking, and segmentation
- Power BI dashboard design
- Business-question framing and recommendation writing
Limitations
- The source report identifies 37 missing values in Review Rating; document how the final notebook handles these values.
- The report lists business questions but does not include every final SQL result, so add verified results and quantified findings before making claims about which group performed best.
- Observational data can show associations but does not, by itself, prove causation.
- The available report does not state profit or cost data, so revenue should not be described as profit.
How to Reproduce
1. Download the dataset from its original source and review its usage terms.
2. Install the Python libraries used in your notebook (for example, pandas and the database connector used by your code).
3. Run the notebook to clean and prepare the data.
4. Create/configure PostgreSQL and load the cleaned table.
5. Run the SQL scripts.
6. Open the Power BI .pbix file and update the data connection if needed.
Add exact installation commands, database/table names, and data-source links once confirmed in your environment.
