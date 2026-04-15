# A/B Testing & Product Analytics

## Project Overview
This project analyzes an A/B test experiment to evaluate differences between a Control and a Treatment variant. The workflow includes data cleaning, exploratory data analysis (EDA), statistical testing, and business insight interpretation to support data-driven product decisions.

## Objectives
- Clean and prepare experiment data for analysis
- Compare Control and Treatment groups across key product metrics
- Analyze user behavior and experiment performance
- Apply statistical testing to evaluate significance
- Summarize findings and provide actionable recommendations

## Dataset
The dataset includes the following columns:

- `user_id`
- `date`
- `variant`
- `device_type`
- `country`
- `new_user`
- `session_duration_min`
- `pages_viewed`
- `added_to_cart`
- `purchase`
- `revenue`

## Data Cleaning
The following preprocessing steps were applied:

- Removed duplicate rows
- Standardized inconsistent categorical values
- Filled missing values in `device_type` using mode
- Filled missing values in `session_duration_min` and `pages_viewed` using median
- Corrected invalid negative values in behavioral metrics
- Converted `date` to datetime format

## Exploratory Data Analysis
The analysis focused on:

- User count by variant
- Purchase rate by variant
- Average revenue by variant
- Average session duration by variant
- User distribution by device type
- Purchase rate by device type and variant
- Revenue by country and variant

## Statistical Testing
The following tests were applied:

- **Chi-square test** for purchase conversion
- **Independent t-test** for revenue
- **Independent t-test** for session duration

### Results
- **Chi-square statistic:** 0.5292  
- **Purchase p-value:** 0.4670  

- **Revenue t-statistic:** 0.8079  
- **Revenue p-value:** 0.4193  

- **Session duration t-statistic:** 3.3147  
- **Session duration p-value:** 0.0009  

## Conclusion
The Treatment variant performed slightly better across several metrics, but only session duration showed a statistically significant improvement. This suggests that the experiment had a positive effect on engagement, while its impact on conversion and revenue remains inconclusive.

## Visualizations

### User Count by Variant
![User Count by Variant](images/user_count_by_variant.jpg)

### Purchase Rate by Variant
![Purchase Rate by Variant](images/purchase_rate_by_variant.jpg)

### Average Revenue by Variant
![Average Revenue by Variant](images/average_revenue_by_variant.jpg)

### Average Session Duration by Variant
![Average Session Duration by Variant](images/average_session_duration_by_variant.jpg)

## Tools and Libraries
- Python
- pandas
- numpy
- matplotlib
- scipy

## Project Structure
```bash
ab-testing-product-analytics/
│
├── data/
│   ├── raw/
│   │   └── ab_testing_product_analytics_raw.csv
│   └── processed/
│       └── ab_testing_product_analytics_cleaned.csv
├── images/
├── notebooks/
├── README.md
└── requirements.txt
```

## Key Insight
The Treatment group showed slightly stronger performance overall, but the only statistically significant improvement was in session duration. This indicates improved engagement, while business impact on purchases and revenue is not yet confirmed.

## Future Improvements
- Test additional product metrics
- Segment results by country, device type, and user type
- Run the experiment longer for stronger statistical power
- Compare results with retention or funnel-based metrics

## Author
Nađa Radojičić
