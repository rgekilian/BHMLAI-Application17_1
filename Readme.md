# BHMLAI-Application17_1: Bank Marketing Campaign

## Data Understanding

the data originates from 17 real-world marketing campaigns carried out by a Portuguese bank with the objective of promoting bank deposit subscriptions. These campaigns, spanning from May 2018 to November 2010, involved interactions with a total of 79,354 contacts. The dataset, already cleaned at its source, is focused on these phone-based marketing campaigns.

Key observations on the dataset:

- There's a significant imbalance between the two classes / labels.
- The dataset is devoid of missing values.

## Business Objective

**Background:**

Amid rising pressures for European banks to escalate their financial assets, an adopted strategy has been to offer long-term deposit applications with competitive interest rates, specifically by launching direct marketing campaigns. The overall business aim is to augment the efficiency of these campaigns for long-term deposit subscriptions by minimizing the required contacts.

**Goal:**

The primary objective of this Machine Learning analysis is to identify a model capable of explaining the success of a contact - whether the client would subscribe to the deposit. A successful model could enhance campaign efficiency by identifying pivotal characteristics influencing success, thereby better managing resources and selecting a high-quality, cost-effective potential customer base.

This is achieved by comparing the performance of k-nearest neighbors, logistic regression, decision trees, and support vector machines.

## Business Impact

The outcome of this project will directly influence the bank's marketing strategies, leading to the following potential benefits:

1. **Cost efficiency**: Predicting the customers who are most likely to subscribe to a term deposit will allow the bank to target these individuals specifically, thus reducing the costs associated with broad spectrum marketing.
2. **Increased conversion rate**: By focusing the marketing efforts on the clients that are predicted to subscribe, the bank can increase the effectiveness of the marketing campaign, resulting in higher conversion rates.
3. **Customer satisfaction**: Properly directed marketing efforts will reduce the number of unwanted contacts for customers that are not interested in the product, leading to higher customer satisfaction.

## Approach

The project will follow the CRISP-DM (Cross-Industry Standard Process for Data Mining) methodology.

The aim is to select the model that gives the highest accuracy while also considering the interpretability of the model, as understanding the factors that influence a client's decision can provide additional insights for the business.

Data Understanding, Data Preparation, Modeling and Evaluation are detailed in the python notebook:

- prompt_III.ipynb

Dataset and Data Dictionary are available:

- /data/bank-additional-full.csv
- /data/bank-additional-names.txt
- /data/bank-additional.csv (subset of the full dataset)

We will make use of the article accompanying the dataset [here](reference/CRISP-DM-BANK.pdf) for more information on the data and features.

## Conclusions

- Due to the heavily unbalanced dataset labels, the model performance is limited. To address this issue, we have chosen the F1 score as the primary performance metric and used AUC to compare the models and make the final selection.
- All models outperformed the baseline, indicating positive outcomes.

- The Decision Tree Classifier emerges as the best model for customer classification, offering potential to classify on both labels.

- The data derived from marketing campaigns appears to lack relevance. Most of the features are not predictive of the outcome. The selected model relying only on the following features:
  - emp.var.rate
  - cons.conf.idx
  - duration
  - nr.employed
  - pdays
  - month
  - age

**Overall conclusion:**

Despite the efforts, the model would be limited as a practical tool for customer classification.

## Next Steps

### Potential improvements to the models could include

In order to improve the model, we could try to gather more information regarding the customers, such as income, and there banking profile as well as trying to reduce the number of unknown values.

### In terms of future campaigns, the bank could consider

- We could also utilize SMOTE to address class imbalance, potentially improving model accuracy. However, we shall monitor for introduction of noise.
