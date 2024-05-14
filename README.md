# Understanding-the-Determinants-of-Adult-Income-in-the-United-States

This study explores the determinants of adult income in the United States using anonymized census data. Analyzing a diverse set of demographic attributes, including age, education, and occupation, alongside income brackets categorized as greater than or less than $50,000, the research seeks to uncover underlying patterns and correlations.

Initiating with meticulous data preprocessing techniques to handle missing values and encode categorical variables, the analysis proceeds with extensive exploratory data analysis (EDA) to unveil intricate relationships between income and demographic factors. Key stages involve the application of feature selection techniques to identify influential predictors for income, leading to the development of robust machine learning models. Leveraging Python libraries, models range from logistic regression to advanced algorithms like decision trees and gradient boosting machines.

Model performance is rigorously assessed through various evaluation metrics and cross-validation methods, with a keen emphasis on model interpretation to discern the underlying drivers of income levels. Further refinement is achieved through meticulous fine-tuning and optimization, culminating in the selection of the most optimal model for deployment, guided by Python-based evaluation techniques.

In conclusion, the study provides valuable insights into the socioeconomic dynamics shaping adult income in the United States.

### Research Question

Can we identify significant relationships between demographic factors (age, education, occupation, etc.) and income levels in the US census data?

### Data Preparation

Data Source: The data for this project will be obtained from the dataset available on Google BigQuery.
https://cloud.google.com/bigquery/public-data/
`bigquery-public-data.ml_datasets.census_adult_income`

Data Collection Method:

- Platform: We will access the data using Google BigQuery.
- Query: We will execute the following SQL query to retrieve the required data:

SELECT * FROM `bigquery-public-data.census_adult_income` LIMIT 32561;

- Download Format: The extracted data will be downloaded in CSV format for further analysis.

### Type of Study

This type of study using census adult income data is an observational study.
Observational studies involve observing existing data without manipulating variables . In this case, we are  analyzing pre-collected census data on demographics and income. We are not assigning individuals to different work schedules, education levels, or income brackets to see the effect on their income.
Observational studies can't definitively establish cause-and-effect relationships.  While we might find correlations between income and other factors like education, we can't say for certain that education directly causes higher income.  There could be other unobserved factors influencing both.

### Variables

The following are the columns present in the dataset - 
- age: This variable is most likely continuous and represents the individual's age in years.

- workclass: This variable is categorical and indicates the type of work of the individual. Examples of possible values include "Private", "Self-employed", "Government", "Without pay", etc.

- functional_weight: This variable is continuous and represents a weighted number of years of education according to an individual's functional status. The meaning of "functional status" in this context might not be explicitly defined in the data documentation and could require further research.

- education: This variable is categorical and indicates the highest level of education attained by the individual. Examples of possible values include "Some College Degree", "9th".

- education_num: This variable is continuous and represents the number of years of education completed by the individual.

- marital_status: This variable is categorical and indicates the marital status of the individual. Examples of possible values include "Married-civ-spouse",, "Never married", etc.

- occupation: This variable is categorical and refers to the usual occupation of the individual. Examples of possible values include "Sales", "Other-Service" etc.

- relationship: This variable is categorical and describes the relationship of the individual to the household head. Examples of possible values include "Wife", "Other relative" etc.

- race: This variable is categorical and indicates the race of the individual. Examples of possible values might include "White", "Black" etc.
- sex: This variable is categorical and indicates the gender of the individual (usually "Male" or "Female").
- capital_gain: This variable is continuous and represents the amount of capital gain (increase in asset value) the individual experienced in the past year.
- capital_loss: This variable is continuous and represents the amount of capital loss (decrease in asset value) the individual experienced in the past year.
- hours_per_week: This variable is continuous and represents the usual number of hours worked per week by the individual in the past year.
- native_country: This variable is categorical and indicates the country of birth of the individual.
- income_bracket: This is the target variable and is categorical. It indicates whether the individual's income falls above or below a certain threshold (e.g., > $50,000 or <= $50,000).

Dependent Variable: Income Bracket (binary: >  $50,000   or <= $50,000)

Independent Variables: 'age', 'workclass', 'functional_weight', 'education', 'education_num',
       'marital_status', 'occupation', 'relationship', 'race', 'sex',
       'capital_gain', 'capital_loss', 'hours_per_week', 'native_country'
