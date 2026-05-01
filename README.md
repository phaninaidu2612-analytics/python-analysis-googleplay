

# Google Play Store App Analysis (EDA + Feature Engineering)
## Dataset Link :
https://raw.githubusercontent.com/krishnaik06/playstore-Dataset/main/googleplaystore.csv

## Project Overview :

This project focuses on performing Exploratory Data Analysis (EDA) and Feature Engineering on the Google Play Store dataset to uncover patterns in app popularity, installs, ratings, and pricing.

The analysis helps understand:

Which app categories are most popular
What factors influence installs and ratings
How pricing and app size affect user engagement

## Problem Statement :

With over 2.5 million apps available on the Google Play Store, understanding what drives app success is critical.

The objective of this project is to:

- Identify the most popular app categories
- Find apps with highest installs and ratings
- Analyze the impact of size, price, and reviews
- Prepare clean and structured data for further analysis

## Dataset Description
Total Rows: 10,841
Total Columns: 20
### Key Features :
- App – Application name
- Category – App category
- Rating – User rating
- Reviews – Number of reviews
- Size – App size (varied formats like “19M”, “Varies with device”)
- Installs – Number of installs (e.g., “1,000+”)
- Type – Free / Paid
- Price – App price
- Content Rating – Age group
- Genres – App genre
- Last Updated / Current Version / Android Version

## Steps Followed :
 1. Data Cleaning
Removed duplicate records
Handled missing values in key columns (Rating, Size, etc.)
Cleaned columns with inconsistent formats:
Installs: removed + and , → converted to numeric
Price: removed $ → converted to numeric
Size: converted from text (M/K) to numeric MB
Standardized categorical values
Dropped irrelevant or inconsistent rows

2. Exploratory Data Analysis (EDA)

Performed analysis using Pandas, Matplotlib, and Seaborn:

- Distribution of app categories
- Most popular categories based on installs
- Relationship between:
- Ratings vs Reviews
- Size vs Installs
- Price vs Installs
#### Identified:
- Top apps by installs
- Category-wise performance
- Free vs Paid app trends

3. Feature Engineering

Created new meaningful features to enhance analysis:

- Installs (Numeric) – Cleaned and converted
- Price (Numeric) – Standardized format
- Size (MB) – Converted into consistent unit

Revenue Approximation:
Revenue = Installs * Price
Rating Category (optional binning):
Low / Medium / High
Log Transformations (for skewed data like installs/reviews)


## Key Insights

### App Popularity
Categories like GAME, FAMILY, and TOOLS dominate in terms of installs
Free apps significantly outperform paid apps in user reach
### Ratings & Reviews
Apps with higher reviews tend to have better ratings
However, some high-install apps still have moderate ratings → indicating mixed user experience
### Price Impact
Most top-performing apps are free
Paid apps generally have lower installs but niche audiences
### Size vs Installs
No strong direct correlation
However, extremely large apps may reduce adoption slightly
### Data Quality Observation
Dataset contains:
Missing values
Inconsistent formats
Mixed data types
Highlighting the importance of data cleaning before analysis

## Tools & Technologies Used :
- Python
- Pandas – Data manipulation
- NumPy – Numerical operations
- Matplotlib / Seaborn – Data visualization
- Jupyter Notebook – Analysis environment


## Conclusion :

This project demonstrates how raw, unstructured app data can be transformed into meaningful insights using data cleaning, exploratory analysis, and feature engineering techniques.

The analysis reveals that app category, pricing strategy, and user engagement (reviews & ratings) are key factors influencing app success on the Google Play Store. While free apps dominate in terms of installs, paid apps cater to more specific user segments.

By applying feature engineering and statistical analysis, the dataset was enhanced to better understand relationships between variables and support deeper insights.

Overall, this project highlights the importance of:

- Data preprocessing and cleaning
- Exploratory analysis to identify trends
- Feature engineering for improved insights

It serves as a strong foundation for building predictive models or recommendation systems in the mobile app ecosystem.

## Source
Google Play Store Dataset (Kaggle / GitHub)
