# Data Mining and Analysis of US Police Shootings: Patterns, Predictions, and Insights

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
The project was implemented in R, leveraging a variety of packages for data manipulation, visualization, and reporting:
- dplyr and tidyr for data wrangling and preparation
- ggplot2 and gridExtra for visualization and arranging plots
- scales for customizing graphical scales
- knitr and kableExtra for creating well-formatted tables and reports
- rcompanion for statistical analysis support


#### Data visualisations
<img width="667" height="422" alt="image" src="https://github.com/user-attachments/assets/acb75cf6-0456-460e-8e9a-9bd5ab119bfa" />


<img width="670" height="392" alt="image" src="https://github.com/user-attachments/assets/73a62caf-e16b-4552-8af1-ea3f5f98dce4" />


<img width="741" height="244" alt="image" src="https://github.com/user-attachments/assets/d95cc424-19c9-4146-9f27-2319bf61012a" />


<img width="626" height="196" alt="image" src="https://github.com/user-attachments/assets/e9706722-5dfe-41a4-a5aa-b4a90eb6fcc4" />


<img width="603" height="226" alt="image" src="https://github.com/user-attachments/assets/e334716b-69d4-4bcf-b6e9-e35cd9fee274" />


<img width="989" height="365" alt="image" src="https://github.com/user-attachments/assets/3d7f7acb-529e-4704-b749-9392753fa5b3" />


<img width="936" height="330" alt="image" src="https://github.com/user-attachments/assets/43792431-a92f-469d-800a-fbd719011502" />









