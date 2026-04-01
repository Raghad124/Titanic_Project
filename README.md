Titanic Data Analysis and Preprocessing Report
Introduction

The purpose of this project is to analyze the Titanic dataset and prepare it for machine learning tasks.
The work was divided into three main phases. The first phase focused on data cleaning, the second phase focused on feature engineering and preprocessing, and the third phase focused on exploratory data analysis and visualization.

These steps are important because they improve data quality, make the dataset easier for machine learning models to understand, and help discover useful patterns related to passenger survival.

Phase 1: Data Cleaning

In the first phase, the Titanic dataset was uploaded and loaded into Google Colab using the pandas library. The first five rows of the dataset were displayed to understand the structure of the data and identify the available columns.

After that, the dataset shape was checked to determine the number of rows and columns. The data types and column information were also reviewed to understand which columns were numerical and which were categorical.

The next step was checking the dataset for missing values and duplicate rows. This was an important process because missing or repeated data can negatively affect the analysis results.

A cleaning function was then created to organize all preprocessing steps in one place.

The following cleaning tasks were completed:

Duplicate rows were removed to avoid repeated information.
The Survived and Pclass columns were converted into categorical data types.
Missing values in the Age column were replaced with the median because it is less sensitive to extreme values.
Missing values in the Embarked column were replaced with the mode since it represents the most frequent category.
The Cabin column was removed because it contained too many missing values.
Extreme values in the Fare column were reduced by capping values above the 99th percentile.

Finally, validation checks were performed to confirm that:

no missing values remained,
all age values were valid,
and the final dataset structure was correct.

This phase ensured that the dataset became clean, consistent, and ready for deeper analysis.

Phase 2: Feature Engineering and Preprocessing

The second phase focused on transforming the cleaned data into a better format for machine learning.

First, missing numerical values in Age and Fare were replaced using the mean.

After that, One-Hot Encoding was applied to the categorical columns Sex and Embarked. This converted text categories into numerical columns that machine learning models can process effectively.

In addition, Ordinal Encoding was conceptually included for any ordered categorical feature. This method converts categories with a natural ranking into numerical values from low to high, which helps the model understand the order between categories.

The numerical columns Age and Fare were then standardized using feature scaling. This step is useful because it places both features on the same scale, improving model performance.

Next, several meaningful new features were created:

Fare per person: this feature represents the ticket cost per family member and may help reveal spending patterns related to survival.
Parch ratio: this feature measures the ratio of parents or children to total family size, which may capture family-related behavior.
Interaction feature: a combined feature was created using passenger class and fare to better represent the relationship between ticket class and price.

A log transformation was then applied to the fare column to reduce skewness and make the distribution closer to normal. The histogram before and after the transformation helped visualize the improvement.

The Age column was also divided into meaningful groups such as New, Recent, and Old, which improves interpretability and can simplify future modeling.

Finally, highly correlated features were identified using a correlation matrix, and one redundant feature was removed to reduce unnecessary repetition in the dataset.

This phase made the data richer, more meaningful, and better prepared for predictive modeling.

Phase 3: Exploratory Data Analysis (EDA)

The final phase focused on understanding the dataset through visual analysis.

First, histograms were created for Age, Fare, and SibSp to study how the values are distributed and to identify skewness or unusual patterns.

Next, a boxplot was used to compare fare distribution across passenger classes while also considering survival status. This helped visualize how higher ticket classes may relate to higher survival rates.

A correlation heatmap was then created to display the top features most strongly related to survival. This visualization made it easier to identify the variables that may have the greatest impact on prediction.

A scatter plot between Age and Fare, colored by survival outcome, was also used to explore possible relationships between age, ticket price, and survival.

Lastly, the average survival rate was calculated for each passenger class. This group summary clearly showed how survival probability differs depending on class level.

This phase provided clear visual insights into the dataset and helped identify patterns that may be useful for machine learning.

Conclusion

In conclusion, this project successfully cleaned, transformed, and explored the Titanic dataset through three well-organized phases.

Phase 1 improved the quality and consistency of the data.
Phase 2 prepared the dataset through encoding, scaling, and feature engineering.
Phase 3 provided visual insights and highlighted important relationships with survival.

Overall, these steps create a strong and reliable foundation for building a machine learning model to predict passenger survival on the Titani
