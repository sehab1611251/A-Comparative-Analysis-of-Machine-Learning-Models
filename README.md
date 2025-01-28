## Project Overview
This project evaluates various machine learning models to predict national happiness levels. The main objectives include:
- Forecasting the **Life Ladder** score (a measure of life satisfaction).
- Classifying happiness levels from "very unhappy" to "very happy."
- Identifying key factors influencing happiness levels.

## Machine Learning Models Used
1. **Multiple Linear Regression**: Models the linear relationship with the Life Ladder score.
2. **Multinomial Logistic Regression**: Handles multi-class classification for happiness levels.
3. **Ridge Regression**: Improves stability by addressing multicollinearity and overfitting.
4. **Polynomial Regression**: Captures non-linear relationships in the data.
5. **Naive Bayes**: Provides a probabilistic framework for classifying happiness levels.

## Dataset Overview
- **Source**: [World Happiness Report](https://worldhappiness.report/data/)
- **Number of Observations**: ~2000
- **Target Variable**: 
  - **Life Ladder**: Continuous measure of self-reported life satisfaction.
- **Key Predictors**:
  - **Social Support**
  - **Healthy Life Expectancy**
  - **Freedom to Make Life Choices**
  - **Perceptions of Corruption**
  - **Positive Affect**
  - **Negative Affect**

### Excluded Features
- **Year**: Temporal variable with no direct relationship to Life Ladder.
- **Generosity**: Weak predictor with limited variability.
- **Log_GDP_per_capita**: Redundant due to high correlation with other predictors.

## Data Processing
1. Standardized column names.
2. Removed missing values.
3. Created a categorical variable `Happiness_Level` based on the median Life Ladder score.
4. Detected and removed influential points using Cook’s Distance.
5. Split the data into training (80%) and testing (20%).

## Results
- **Regression Models**:
  - **Polynomial Regression**: Best RMSE = 0.54.
  - **Multiple Linear Regression**: RMSE = 0.59.
  - **Ridge Regression**: RMSE = 0.58.
- **Classification Models**:
  - **Multinomial Logistic Regression**: Accuracy = 65%.
  - **Naive Bayes**: Accuracy = 64%.

## Key Insights
- **Healthy Life Expectancy**: Most significant predictor across all models.
- **Social Support and Positive Affect**: Consistently impactful predictors.

## Example Inputs and Outputs
### Multiple Linear Regression
Input:
- Social Support, Healthy Life Expectancy, Positive Affect

Output:
- Predicted Life Ladder score: 6.8

### Multinomial Logistic Regression
Input:
- Social Support, Freedom to Make Life Choices, Perceptions of Corruption

Output:
- Happiness Level: Very Happy

## Conclusion
- Polynomial Regression demonstrated the best regression performance.
- Multinomial Logistic Regression outperformed Naive Bayes for classification tasks.

---

Thank you for exploring this project! For further details, feel free to review the source code and dataset.

