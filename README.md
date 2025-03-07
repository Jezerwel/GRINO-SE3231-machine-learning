# Linear Regression Model Conclusion

The linear regression model using "Playing Hours" as a single predictor demonstrates very weak predictive power. The model's Mean Squared Error (MSE) and low R² score of 0.04 indicate that only 4% of the variance in grades can be explained by playing hours alone. The scatter plot visualization shows a wide dispersion of points around the regression line which
indicates that "Playing Hours" alone is not a strong predictor of grades, and other factors likely
play a significant role.

# Multiple Linear Regression Model Conclusion

The multiple linear regression model, incorporating several features, shows an improvement over the single-variable linear regression. The R² score on the test data is 0.2557, indicating that approximately 25.57% of the variance in grades is explained by the included features. The scatter plot visualization reveals an interesting pattern: the actual grades (blue) align perfectly along the diagonal "Perfect Fit" line, while the predicted grades (red) display considerable scatter around this line, particularly in the higher grade ranges (60-90+). This suggests that the model struggles with predicting grades that are below 60. The sorted feature coefficients shows the relative impact of each feature on grade prediction. "Mother Education" and "Father Education" have positive coefficients, suggesting a positive correlation with grades, while "Playing Games" has a negative coefficient, indicating negative correlation. Although this model performs better than the single-variable model, the scattered prediction points indicate that there is still a significant portion of the variance in grades that remains unexplained, suggesting that additional factors or a more complex model might be needed for better predictive accuracy.

# Answers to Questions about the Dataset and Linear Regression

## 1. Why did you choose this dataset?

The dataset "gameandgrade.csv" was chosen because I am also a gamer and it is interesting to explore the relationship between various factors related to gaming habits and academic performance (grades). The dataset includes features such as "Playing Hours," "Playing Games," parental education and revenue, and other factors that could potentially influence a student's grade. This allows for an analysis of how well these gaming-related variables can predict or explain the variance in student grades, making it an interesting dataset.

## 2. What is your conclusion upon conducting linear regression on this dataset?

After conducting linear regression analysis, the conclusion is that while there is some degree of correlation between the features in the dataset and the grades, the models have limited predictive power. The simple linear regression model, using only "Playing Hours," explains only a small fraction of the variance in grades, as indicated by a low R² score. The multiple linear regression model, which incorporates several features, shows an improvement but still leaves a significant portion of the variance unexplained. This suggests that gaming habits, parental education, and revenue, as represented in this dataset, are not strong predictors of academic performance when used in a linear regression model. Other factors not included in the dataset might play a more significant role in determining student grades.

## 3. How relevant is linear regression today?

Linear regression remains highly relevant today, despite its simplicity compared to more complex machine learning algorithms. It is still widely used for several reasons:

- **Interpretability:** Linear regression models are easy to interpret, providing clear insights into the relationship between predictors and the target variable.
- **Baseline Model:** It's useful baseline model to compare against more complex algorithms.
- **Simplicity:** Linear regression is computationally efficient and easy to implement, making it suitable for quick analyses.
- **Foundation:** It forms the foundation for more advanced techniques, such as generalized linear models and regularization methods.
- **Specific Use Cases:** In scenarios where the relationship between variables is approximately linear, and interpretability is important, linear regression is the preferred choice.

While it may not always provide the highest accuracy for complex, nonlinear relationships, its simplicity, interpretability, and efficiency makes it still relevant today.
