# Fraud Risk Analysis \& Transaction Monitoring



##### Project Overview



This project investigates fraud patterns in synthetic mobile-money transactions and evaluates how simple rule-based monitoring scenarios perform at different transaction amount thresholds.



Using SQL and Python, the analysis explores transaction types, measures fraud detection performance, and examines the trade-off between identifying fraudulent transactions and generating false-positive alerts.



##### Business Question



Can simple transaction-monitoring rules identify suspicious activity effectively while keeping alert volumes manageable?



##### Tools \& Technologies



* SQL / SQLite: Transaction profiling and aggregation
* Python: Analysis and evaluation
* Pandas: Data manipulation
* Matplotlib: Data visualization
* scikit-learn: Classification metrics



##### Dataset



The project uses the synthetic PaySim mobile-money transaction dataset.



Dataset source: "PaySim — Kaggle" (https://www.kaggle.com/datasets/ealaxi/paysim1)



The dataset is not included in this repository. Download it from Kaggle and follow the notebook instructions to reproduce the analysis.



##### Methodology



1. Profile transaction types, volumes, amounts, and observed fraud rates.
2. Inspect data quality, including missing values and duplicate records.
3. Develop a rule flagging TRANSFER and CASH\_OUT transactions above a specified amount threshold.
4. Compare five amount thresholds: 50,000, 100,000, 200,000, 500,000, and 1,000,000.
5. Evaluate precision, recall, false-positive rate, missed fraud, and alert volume.
6. Interpret the results in terms of fraud detection and investigation workload.



##### Key Findings



* TRANSFER had the highest observed fraud rate at 0.7688%.
* CASH\_OUT had the highest observed fraud count, with 4,116 cases.
* At a threshold of 50,000, the rule achieved 87.36% recall, but generated approximately 2.36 million alerts.
* At a threshold of 1,000,000, precision increased to 2.07%, while recall decreased to 32.95% and alert volume fell to 130,507.



These results demonstrate the trade-off between detecting a larger share of fraud and reducing the number of transactions sent for investigation.



##### Limitations



* PaySim is synthetic data, so the results may not generalize to real financial transactions.
* The tested amount thresholds are illustrative and have not been validated against real investigation costs or business requirements.
* The analysis evaluates a small set of rules and is not a deployed fraud detection system.
* Observed fraud patterns should not be interpreted as proof that transaction types with no recorded fraud are inherently risk-free.



##### Future Improvements



* Evaluate account balance changes as additional risk indicators.
* Compare alternative rule combinations.
* Estimate alert workload under different operational constraints.
* Investigate whether transaction behaviour can improve detection performance.





Data analysis portfolio project demonstrating SQL, Python, fraud-risk investigation, and performance evaluation.

