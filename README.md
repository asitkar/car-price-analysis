# What Drives the Price of a Car?
**An Application of the CRISP-DM Framework for Used Car Dealership Inventory Optimization**

## Executive Summary & Findings
This analysis provides data-driven recommendations to a used car dealership looking to fine-tune its inventory acquisition and pricing strategy. Based on an analysis of over 420K used car listings, the following key insights were identified:

### Actionable Strategic Insights
* **The Mileage Penalty:** Every addition of 10,000 miles on the odometer decreases the vehicle value predictably. Inventory velocity should prioritize lower-mileage vehicles (under 80,000 miles) where premium margins exist.
* **Vehicle Type and Drive Command Premium:** Pickups and SUVs consistently command significantly higher price baselines compared to sedans and hatchbacks. Four-wheel drive (4wd) configurations significantly outperform front-wheel drive options across almost all categories.
* **Fuel Type Impact:** Diesel and electric vehicles exhibit distinct structural pricing behaviors; diesel options retain strong premiums in commercial and pickup categories.

## Technical Methodology
The project was executed following the **CRISP-DM** lifecycle:
1. **Business Understanding:** Establish pricing determinants to minimize inventory holding costs.
2. **Data Understanding:** Explored categorical impacts (manufacturer, title status) and parsed quantitative indicators.
3. **Data Preparation:** Removed severe outliers (e.g., cars priced under \$500 or over \$100,000), imputed missing attributes, scaled numerical entries, and applied One-Hot Encoding to categories.
4. **Modeling:** Trained Linear Regression, Ridge, and Lasso configurations utilizing a 5-fold cross-validated `GridSearchCV` pipeline.
5. **Evaluation:** Models were benchmarked using Root Mean Squared Error (RMSE) to flag and penalize severe mispricing discrepancies.

## Key Visualizations & Jupyter Notebook
The full data engineering pipeline, statistical evaluations, and exploratory charts are documented in the interactive notebook.

👉 **[Link to Jupyter Notebook](./notebooks/car_price_analysis.ipynb)**

## Recommendations & Next Steps
* **Target Inventory Acquisition:** Focus procurement efforts on trucks, pickups, and SUVs with clean title histories, avoiding vehicles with missing or salvaged documentation.
* **Dynamic Depreciation Pricing:** Implement an automated baseline markdown schedule tied directly to odometer thresholds to accelerate turning inventory over.
