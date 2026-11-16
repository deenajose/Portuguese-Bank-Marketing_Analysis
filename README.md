# Portuguese Bank Marketing

## Project Overview

This project analyzes historical direct marketing campaigns for term deposits at a Portuguese bank. It explores customer and campaign patterns, compares predictive models, and develops recommendations for prioritizing outreach.

## Dataset

The analysis uses `bank-additional-full.csv`, covering campaigns from May 2008 to November 2010. After removing 12 exact duplicate records, the dataset contains 41,176 rows. About 11.3% of customers subscribed.

## Approach

The notebook performs data quality checks and exploratory analysis, then compares Logistic Regression, Decision Tree, Random Forest, Extra Trees, AdaBoost, and Gradient Boosting models. It uses cross-validation and tuning, with call duration excluded from pre-call production candidates because it is only known after a call.

## Results

The tuned Random Forest was selected using cross-validation. On the held-out test set, it achieved 0.489 average precision and 0.812 ROC-AUC. Ranking the top 20% of customers captured about 66% of test-set subscribers. The leading models performed similarly, so the recommendation should be treated as a candidate for a controlled pilot.

## Recommendations

Test outreach to customers with prior campaign success, evaluate cellular contact and promising customer groups, and use model scores to prioritize calls. Validate these findings on recent campaign data before broader use; the dataset is historical.

## Notebook

Open `Portuguese_Bank_Marketing.ipynb` to review the full analysis, model comparison, and recommendations.
