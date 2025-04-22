# IS6813_Group_Capstone
IS 6813 - Group Capstone - Spring 2025

# Group 6 MSBA Capstone Project
## Summary of Approach & Recommendations

### Initial Approach: Growth Characteristics
We first attempted supervised and unsupervised models to find provided or engineered features correlated with growth from 2023-2024.

### Revised Approach: HTE Modeling
With few and not strong results from the initial models, we changed our approach to explore an interesting finding that some frequent order types correlated with growth in sales and others with declining sales.

We pivoted to looking at the data as an observational study where the "treatment" was certain frequent order types correlated with growth and the "control" was the other types. Since this is customer behavior, their choices that land them in the "treatment" vs "control" groups are subject to potential confounding bias.

Basic treatment effect (TE) modeling allows for estimation of average treatment effects (ATEs) across the entire sample. On the other hand, Heterogenous Treatment Effect (HTE) modeling both handles potential bias and allows estimation of a TE for individuals or sub-groups. We could therefore calculate individual treatment effects (ITEs) per customer and aggregate them into conditional average treatment effects (CATEs) for sub-groups, such as members of a specific trade channel.

### Recommendations:
Swire Coca-Cola (SCC) utilize HTE modeling for frequent order type and other customer behaviors as a complement to their delivery standardization process. Other groups suggested a variety of thresholds or decision criteria for SCC, but our group advises that customers which do not meet SCC's criteria to continue on red truck delivery might be subject to targeted intervention to improve their outcomes prior to being swapped to white truck.

We conclude that our work demonstrates the usefulness of the HTE modeling technique and our presentation shows how the results can be utilized to target customers individually or by groups. However, our R-squared for the best HTE model was relatively low, and therefore we presented our value as a "proof-of-concept" and do not recommend SCC use our exact results or expect the estimate ITEs or CATEs to be accurate for the customers and trade channels presented.


## Document List

1. Business Problem Statement
Summary of problem and our original plans for the analytic approach.
(Provided in .pdf format)

2. EDA Notebook
Exploratory data analysis, feature engineering, and cleaning of the data to create the dataset used for modeling.
(Provided in .html and .rmd formats)

3. Modeling Notebook
Initial approach looking for customer characteristics that correspond to growth. Attempted models are as follows:
- Logistic Regression
- Penalized Regression (Lasso and Ridge)
- XG Boost
- Random Forest
- Causal Forest
- Partition Clustering (k-means and k-medoid)
- DBSCAN Clustering (with Random Forest for variable contribution to clusters)
(Provided in .pdf format only, due to a mix of R and python code)

4. Additional Modeling Notebook 1
This notebook was created after pivot in approach. In the section of this notebook titled "Next Steps: Modeling for Sales Rep Impact", a T-learner was performed for HTE, followed by Random Forest and Lasso Regression models on the ITE values to determine which features correlated with high treatment effects.
(Provided in .html and .ipynb formats)

5. Additional Modeling Notebook 2
The section "Additional Exploration" explores the results found from initial modeling notebook. Following that, we pivoted to TE modeling, and matching and linear regression were paired to estimate ATE, then causal forest to estimate ITEs. The final section "Quantify Benefit from HTE T-learner Model" uses the data from "Additional Modeling Notebook 1" and includes the calculations for the Impact & Targeted Interventions presented in the slides.
(Provided in .html and .rmd formats)

6. Customer Optimization Presentation
Slides as presented to SCC on 16 April 2025.
(Provided in .pdf format)
