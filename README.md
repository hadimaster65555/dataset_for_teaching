# Dataset for Teaching

A personal collection of datasets I use for data-science mentoring sessions, workshops, and self-study — and everything I hand out to mentees for practice. Most folders come with a short `context.txt` or `metadata.txt` that explains the columns and the question the data was meant to answer, so you can start modeling without guesswork.

**60 datasets · 121 CSV files · ~615 MB · plain CSV, one folder per topic.**

Feel free to fork this repo or use any dataset for your own projects!

## At a glance

| | |
|---|---|
| **Datasets** | 60 folders under `dataset/`, one per topic |
| **Files** | 121 CSV files (~615 MB total) |
| **Documentation** | 15 datasets ship with a `context.txt`/`metadata.txt`, a data dictionary, or a problem statement |
| **Categories** | Customer analytics · marketing · A/B testing · causal inference · finance & credit · HR · e-commerce & retail · time series · regression · classification · deep learning & LLM · statistics |
| **Maintained since** | 2022 |

## Repository structure

```
dataset_for_teaching/
└── dataset/
    ├── 50_startups/
    │   └── 50_Startups.csv
    ├── bank_churn_dataset/
    │   ├── bank_churn_data.csv
    │   └── context.txt
    ├── olist_ecommerce_data/
    │   ├── olist_customers_dataset.csv
    │   └── ... (9 relational tables)
    ├── time_series_data/
    │   ├── air_passanger_data/
    │   ├── amazon_stocks_data/
    │   └── ... (8 sub-datasets)
    └── ... (one folder per dataset)
```

Every dataset lives in its own folder under `dataset/`. Folders with supporting notes keep them next to the data.

## Dataset catalog

### Customer analytics — churn, retention & segmentation

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Bank credit-card churn | `bank_churn_dataset` | CSV + context | ~10k credit-card customers: demographics, activity, transaction behavior, attrition label. | Churn classification, imbalanced data |
| Churn modelling | `bank_churn_dataset_2` | CSV | The classic `Churn_Modelling.csv`: 10k bank customers with credit score, geography, balance, exit flag. | Churn modeling, ANN/MLP practice |
| Churn risk (HackerRank) | `churn_risk_rate_hackerank` | train/test CSV | Customer churn-risk competition data with train/test split and sample submission. | Competition-style churn modeling |
| B2B customer churn | `customer_churn` | CSV | Customer spend across the last 4 weeks with a churn flag. | Churn from time-windowed spend features |
| Retail retention | `customer_retention_at_retail_business` | CSV | Customer lifecycle dates, email engagement, order frequency, retained flag. | Retention analysis, RFM, SQL practice |
| Telecom churn | `telco_customer_churn` | CSV | Classic Telco Customer Churn: services, contract, charges, churn label. | Churn classification, model comparison |
| Customer segmentation | `customer_segmentation_profile_dataset` | CSV | Credit-card customers with income, debt, education, and default status. | Clustering, segmentation, PCA |

### Marketing, campaigns & customer experience

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Bank marketing | `bank_marketing_dataset` | CSV + metadata | Direct phone-campaign data from a Portuguese bank (~41k contacts, 20 features). | Campaign response prediction, data-leakage discussion (`duration`) |
| Campaign interactions | `campaign_data` | CSV (~46 MB) | Cookie-level impressions, conversions, and value across marketing channels. | Multi-channel attribution, funnel analysis |
| Email marketing | `email_marketing_data` | train/test CSV | Customer attributes plus three email variants and a conversion flag. | Uplift modeling, treatment-effect analysis |
| Children's clothing spending | `jackjill_clothing_child_clothing_sales` | CSV | Household spending on children's clothing vs household profile (income, education, employment). | Regression with categorical predictors |
| Marketing campaign experiment | `marketing_campaign_experiment` | CSV | Users, channels, personalization variants, conversion, subscription and cancellation dates. | Conversion funnels, experiment readout |
| Campaign response model | `marketing_campaign_response_model` | CSV + metadata | Customer profiles with acceptance across six past campaigns. | Response modeling, profit-maximizing targeting |
| Promotion uplift | `marketing_promotion_uplift_modeling` | CSV | Customer history, channel, offer type (discount/BOGO/none), conversion. | Uplift modeling, promotion targeting |
| Olist marketing funnel | `olist_marketing_funnel_dataset` | 2 CSVs | Marketing qualified leads and closed deals from the Olist marketplace. | Funnel conversion analysis |

### A/B testing & experiments

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Landing page A/B test | `landing_page_experiment` | CSV | A/B test of a landing page with group and converted columns. | Hypothesis testing, power analysis |
| Simulated feature experiment | `simulated_feature_experiment` | CSV | Simulated rollout: treated flag, time in product, purchases, revenue, CTR. | Experiment analysis, variance reduction |
| Website A/B test | `website_ab_testing_data` | CSV | Variants A/B with conversion, length of stay, and revenue. | A/B tests with binary + continuous metrics |

### Causal inference

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Causal impact starter set | `causal_impact_dataset` | 3 mini-datasets + context | Three scenarios: campaign vs. control, inhaler clinical trial, org change impact on sales. | CausalImpact / interrupted time series practice |
| Worker's comp policy (DiD) | `injury_policy` | CSV + context | Kentucky's 1980 benefit-cap change; logged duration of worker's comp benefits. | Difference-in-differences |
| Mosquito nets | `mosquito_nets.csv` | CSV + context | Household malaria risk vs. net usage, program eligibility, income, resistance. | Observational causal inference, confounding |
| Chickens & eggs | `chicken_eggs` | CSV + context | Annual US chicken population and egg production, 1930–1983. | Time series + supply/demand reasoning |
| Learning mindset | `learning_mindset` | CSV | School-level field experiment on a mindset intervention and student achievement. | Causal inference on a real RCT, multilevel data |

### Finance, credit & insurance

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Give Me Some Credit | `GiveMeSomeCredit` | train/test CSV + data dictionary | ~150k borrowers with serious-delinquency target. | Credit risk scoring, class imbalance |
| German credit | `german_credit_datasets` | CSV | The classic UCI German credit risk data. | Interpretable credit classification |
| Car insurance fraud | `car_insurance_fraud_dataset` | CSV + metadata | Claims with policy, incident, and fraud-reported fields. | Fraud classification, feature engineering |
| Insurance claims | `insurance_claim_data` | 3 CSVs | Claims transactions with agents and vendors. | Claims analytics, relational joins |
| Bank customers & transactions | `bank_transaction_investment_dataset` | 3 CSVs + metadata | Synthetic customers, transactions/investments, and branch performance — with noise and missing values. | Joins, cleaning, financial analysis |
| 50 Startups | `50_startups` | CSV | The classic startup profit dataset (R&D, admin, marketing spend → profit). | Intro regression, dummy variables |

### HR & people analytics

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Employee turnover (survival) | `employee_turnover` | CSV | Personnel records with personality scores and a leave-event flag (`stag`, `event`). | Survival analysis, turnover prediction |
| HR analytics turnover | `hr_analytics_turnover_dataset` | CSV | The classic `HR_comma_sep.csv`: ~15k employees with satisfaction, salary, turnover. | Quick ML practice, classification |
| IBM HR attrition | `hr_attrition_dataset` | CSV | IBM's HR employee attrition set (1,470 rows, 35 features). | Explainable attrition modeling, imbalance |
| HR turnover with missing values | `hr_turnover_analytics_miss` | CSV | The turnover dataset with deliberately missing values. | Data cleaning, imputation exercises |
| QueBIT turnover | `quebit_turnover_dataset` | CSV + problem statement + data description | HR turnover data with a written problem statement and dictionary. | Guided end-to-end project |

### E-commerce & retail

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Olist marketplace | `olist_ecommerce_data` | 9 CSVs | Brazilian e-commerce: orders, items, payments, reviews, products, sellers, geolocation. | SQL practice, relational analysis, delivery/review analytics |
| Global superstore | `superstore_dataset` | CSV | Global Superstore orders with products, customers, and profit. | BI dashboards, retail analytics |
| Retail analytics | `retail_data_analytics` | 3 CSVs | Weekly department sales with features and store metadata. | Sales analysis with joins |
| Online retail (UCI) | `ecommerce` | CSV (~44 MB) | UK online retailer invoices: product, quantity, price, customer, country. | RFM, cohort analysis, data cleaning |
| E-commerce 2019 monthly | `ecommerce_time_series_analysis` | 12 CSVs | One file per month of 2019 orders (product, price, order date, address). | Time series resampling, seasonality |
| Future sales | `sales_prediction` | 6 CSVs | Kaggle "Predict Future Sales": daily sales, items, shops, categories. | Demand forecasting, competition practice |
| Office supply orders | `customer_order_data` | CSV | Equipment orders with requester role, quantity, price, and total. | Regression on order value |
| Google Analytics sample | `google_analytics_sample_data` | CSV (~70 MB) | Session-level web analytics: traffic, device, campaign, channel grouping. | Web analytics, large-file aggregation |

### Time series

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Time series pack | `time_series_data` | 8 sub-datasets | Air passengers, Amazon & Google stocks, Amtrak ridership, Australian beer sales, daily website visitors, e-commerce baskets, Superstore. | Classic forecasting practice |
| Walmart store sales | `walmart_store_sales` | CSV + context | Weekly store sales with holidays, temperature, fuel price, CPI, unemployment. | Forecasting with exogenous variables |
| Ice cream sales | `ice_cream_sales_data` | train/test CSV | Sales vs. temperature, price, cost, and weekday. | Intro regression, train/test split |
| Egg sales | `eggs_sales` | CSV | Weekly egg case sales with Easter flags and related commodity prices. | Regression with seasonality, price elasticity |
| Elon Musk tweets / Dogecoin | `elon_musk_tweet` | 3 CSVs | Dogecoin price series and minute-level Tesla vs. S&P 500 data. | Event studies, market data handling |

### Regression & housing

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| California housing | `california_housing` | CSV | California districts with median house value. | Regression baselines |
| Ames housing | `house-prices-advanced-regression-techniques` | train/test CSV + description | Kaggle House Prices competition data with full data description. | Feature engineering, regularized regression |
| Simulated linear data | `linear_regression_simulation_data` | CSV | Simulated data for linear regression demos. | Teaching OLS assumptions |

### Classification & general ML practice

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Breast cancer | `cancer` | CSV + description | Wisconsin Diagnostic Breast Cancer (569 samples, 30 features). | Binary classification teaching |
| Smoking & health | `smoking_data` | CSV | UK lifestyle survey data with smoking status and amounts. | Classification + statistical inference |
| Social network ads | `social_network_ads_dataset` | CSV | 400 users: age, estimated salary, purchase flag. | Classification, decision boundaries |
| Mall customers | `mall_customers` | CSV | The classic 200 mall customers: income vs. spending score. | K-means clustering, segmentation |
| Country development | `country_dataset` | CSV + data dictionary | Country development indicators (mortality, income, fertility, …). | PCA, clustering, dimension reduction |

### Deep learning & LLM

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Digit recognizer | `dataset_for_deep_learning` | train/test CSV + zip | MNIST-style handwritten digits (42k train / 28k test). | Neural networks / CNN practice |
| Vision Pro Q&A | `dataset_for_llm` | CSV | Question–answer pairs about the Apple Vision Pro. | LLM fine-tuning / instruction data demos |

### Statistics & teaching examples

| Dataset | Folder | Files | Description | Good for |
|---|---|---|---|---|
| Stats miscellany | `stats_data` | 6 CSVs | Small classroom sets: sleep study, tip/joke experiment, class data, pass scores, simulations. | Intro statistics, hypothesis testing |
| Indonesia COVID-19 | `indocovid19` | CSV | Daily new/cumulative cases, in-care counts, and deaths for Indonesia. | Local case study, time series basics |
| Sulawesi hotspots | `sulawesi_hotspot_data` | CSV | NASA FIRMS hotspots (latitude, longitude, date) for Sulawesi, 2016–2018. | Geospatial mapping (semicolon-separated CSV) |

## Documentation inside folders

Read the docs file before modeling — they explain columns and quirks:

- `context.txt` / `metadata.txt` — background, column meanings, target variable, caveats (e.g. `bank_marketing_dataset`, `injury_policy`, `mosquito_nets.csv`).
- Data dictionaries — `GiveMeSomeCredit/Data Dictionary.xls`, `country_dataset/data-dictionary.csv`, `quebit_turnover_dataset/dataset_description.xlsx`.
- Descriptions — `cancer/data_description.txt`, `house-prices-advanced-regression-techniques/data_description.txt`.
- Problem statements — e.g. `quebit_turnover_dataset/Problem Statement.docx`.

## Contributing & forks

This repo is meant to be forked and reused.

- **Fork & use:** pick any dataset folder and copy it into your project.
- **Add a dataset:** create a folder under `dataset/` named after the dataset (snake_case) and include:
  - the data file(s) — plain CSV preferred;
  - a `context.txt` or `metadata.txt` describing the source, columns, target, and quirks (missing rows, train/test structure). The existing folders are good templates.
- **Pull requests:** welcome, though this repo is mainly curated for my own mentoring sessions.

## License & attribution

These datasets are collected from public sources — Kaggle, UCI, government open data, textbooks, and other public repositories — for educational and mentoring use. **This repo is not the original source of most data.**

- Licensing varies per dataset. Before using any dataset in production, research, or a commercial product, check the terms on the original source.
- Cite original authors where required.
- Some folders contain synthetic or simulated data (e.g. `bank_transaction_investment_dataset`, `simulated_feature_experiment`) — great for practice, not for real-world conclusions.

No warranty of any kind is provided. Use at your own risk.
