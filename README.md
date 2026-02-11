# Amazon Product Exploratory Data Analysis
An exploratory data analysis (EDA) of Amazon products to uncover the relationships between pricing, consumer ratings, and category trends that drive e-commerce success.

## Project Overview
This project analyzes a comprehensive dataset of over 1000 Amazon products to understand what drives success in the world’s largest e-commerce ecosystem. By examining the interplay between **pricing**, **discounts**, and **customer sentiment**, we identify actionable insights for sellers and market analysts.

## Key Insights
* **Pricing Elasticity:** Analyzed how price fluctuations impact product ratings.
* **Review Significance:** Discovered the "trust threshold"—the number of reviews needed before a rating stabilizes.
* **Category Performance:** Identified which product categories command the highest loyalty and which are most prone to negative feedback.

## Tech Stack
* **Language:** Python
* **Libraries:**
    * `Pandas` (Data Manipulation)
    * `NumPy` (Numerical Processing)
    * `Matplotlib` & `Seaborn` (Data Visualization)

## Dataset Structure
The analysis is performed on a dataset containing the following features:
| Column | Description |
| :--- | :--- |
| **product_id** | Unique identifier for the product |
| **product_name** | Name of the product |
| **category** | Category hierarchy |
| **discounted_price** | The current selling price |
| **actual_price** | The original retail price |
| **discount_percentage** | The percentage of discount offered |
| **rating** | Average user rating |
| **rating_count** | Number of people who voted for the rating |
| **about_product** | Product description |
| **user_id/name** | Reviewer identification |
| **review_id/title/content** | Detailed customer feedback and sentiment |
| **img_link/product_link** | Visual and web references |

## Methodology
1. **Data Cleaning:** Handled missing values, standardized currency formats, and removed duplicates.
2. **Univariate Analysis:** Explored the distribution of prices and ratings using histograms and box plots.
3. **Bivariate Analysis:** Investigated correlations between discounts and sales volume.
4. **Multivariate Analysis:** Visualized category-wise performance using heatmaps and facet grids.

## Analysis Results
* **Discount Percentage vs. Product Rating:** Products that have a higher discount percentage does not neccessarily correlate to a higher customer rating. The distribution for these two features, is in fact, close to being uniform.
* **Discount Price vs. Product Rating:** Cheaper products have the most volatility (more 2.0–3.0 star reviews), whereas higher priced products generally have higher ratings. This is likely because customers have higher expectations that are being met at those higher price points, and those products also maintain a higher baseline of quality.
* **5-Star Reliability Adjustment: Raw vs. Weighted:** My analysis revealed that raw ratings are highly volatile for products with low review counts. By applying a Bayesian weighted scoring system, I normalized the distribution (as seen in the KDE plot). This shifted the rating average to approximately 4.1 and eliminated the construct of 5-star "perfect "products that lacked sufficient social proof.

