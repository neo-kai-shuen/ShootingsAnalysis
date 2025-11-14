# Analysis of shootings records

## University of Arizona - INFO523 Data Mining and Discovery

#### Problem
Police shootings in the United States involve complex patterns related to victim demographics and circumstances, but the relationship between race and weapon type remains unclear. This study analyzes 8,720 fatal police shootings to explore demographic trends, examine potential associations between race and weapon used, and identify patterns through predictive modeling and clustering techniques. Understanding these patterns is crucial for informing policy, improving public safety, and highlighting demographic trends in police use-of-force incidents.


#### Data source
The analysis uses a dataset of 8,720 police shootings in the US, each with 19 attributes covering demographics, incident details, location, and agency information. Key attributes for analysis include gender, threat type, flee status, weapon used, age, and race. Missing location data were largely imputed using external US cities data, and only complete records for the selected attributes were retained. Attributes were classified as numeric, nominal, or binary, and the state attribute was used to standardize location for regional analysis.


#### Approach
The analysis followed a multi-step data mining workflow on 8,720 US police shooting records. Key steps included:
1. Data Exploration & Preprocessing: Summary statistics, handling missing values, and correlation analyses (Pearson’s and Chi-Squared tests).
2. Association Analysis: Mining frequent itemsets with the Apriori algorithm and generating association rules.
3. Predictive Modeling: Building Random Forest and Decision Tree models to predict victim race based on selected attributes.
4. Clustering: Applying PAM and OPTICS algorithms to identify patterns in the data.
5. Outlier Detection: Identifying univariate, multivariate, and contextual outliers to examine unusual cases.

This approach combined statistical analysis, machine learning, and clustering to uncover patterns and relationships in police shooting incidents.


#### Key results
Analysis of 8,720 US police shootings revealed that the majority of victims are male (95.6%), typically aged 41–50, with White (43%), Black (23%), and Hispanic (15.1%) being the most common racial groups. Guns and knives were the most frequently used weapons, and a small proportion of victims were unarmed (5.7% males, 9.6% females).

Correlation analysis showed no strong relationship between race and weapon type (Cramer’s V = 0.07), supporting the null hypothesis. Association rule mining highlighted that the most consistent pattern for both genders was male victims armed with guns, especially in shooting incidents.

Predictive modeling with Random Forest achieved 56% accuracy in predicting race, with age and region as the most important features, while gender and month had little predictive value. Decision Tree analysis further revealed that all Black victims were under 26.

Clustering using PAM and OPTICS identified one large cluster of white male victims armed with guns, with OPTICS producing purer clusters. Outlier analysis detected global, contextual, and collective outliers, including rare racial occurrences in specific states and unusual age clusters, while Mahalanobis distance highlighted multivariate outliers mainly due to geographic distribution.

Overall, the dataset shows clear demographic and weapon patterns but no strong correlation between race and weapon, emphasizing the predominance of young male victims, often armed with guns.


#### Conclusion
Analysis of the US police shooting dataset found no strong correlation between race and weapon used, while clustering revealed that white male victims armed with guns form the majority pattern. Future work includes exploring correlations among other attributes, improving prediction model accuracy, and integrating insights from association rules to enhance modeling. Methodological improvements, such as using Kulc and Imbalance measures for association rules and identifying contextual outliers, strengthened the analysis and provide directions for further research.


#### Technical stack



#### Data visualisations





#### References
- To view dataset: [fatal-police-shootings-data.csv](https://github.com/kai-shuen-neo/dm-ShootingsRecords/blob/main/fatal-police-shootings-data.csv)
- To view code: [analysis.R](https://github.com/kai-shuen-neo/dm-ShootingsRecords/blob/main/analysis.R)
- To view report: [Final_Report_Group_8.pdf](https://github.com/kai-shuen-neo/dm-ShootingsRecords/blob/main/Final_Report_Group_8.pdf)

