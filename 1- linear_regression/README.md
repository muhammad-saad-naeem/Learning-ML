# Project Overview: Manual Feature Selection vs. PCA for Stock Price Prediction

## Objective

This project aims to predict Tesla's (TSLA) stock closing price using a linear regression model, with a primary focus on data analysis and feature selection. The goal is to determine the most effective feature set for accurate stock price predictions and evaluate the performance of manual feature selection against Principal Component Analysis (PCA).

## Summary of Approach

- **Data Analysis and Collinearity Check**: Identified high collinearity among key features ('Open,' 'Low,' 'High,' 'Adj Close') and selected one for further analysis.
- **Manual Feature Selection**: Tested various feature combinations using `itertools.combinations` and evaluated model performance based on error metrics (RMSE) and residual plots.
- **PCA Application**: Applied PCA to reduce dimensionality and compared the performance of PCA-transformed features against the manually selected feature sets.

## Data Analysis

### Feature Correlation

Initially, I analyzed the correlation among features such as 'Open,' 'Low,' 'High,' and 'Adj Close,' which exhibited high collinearity with correlation values nearing 0.99. This high collinearity necessitated careful consideration of which features to include in the model.

### Manual Feature Selection

Using Python's `itertools.combinations`, I manually tested various combinations of these features. Here are some key findings:

- **Volume Feature**: Notably, 'Volume' was the only feature not highly collinear with the others. Despite this, including 'Volume' in the feature combinations did not consistently minimize the error. In fact, the addition of 'Volume' often slightly increased the RMSE, suggesting it might not always add significant predictive value.

- **Price-Related Features**: Combinations of price-related features ('Open,' 'Low,' 'High') generally resulted in lower RMSE, indicating better predictive accuracy. Even though minimal differences in RMSE were observed across combinations, residual plots showed patterns that hinted at the need for further refinement.

I ultimately selected a feature combination that had a slightly higher error but provided a marginally better residual plot.

## Principal Component Analysis (PCA)

To complement the manual feature selection process, PCA was applied to reduce the feature set. While PCA was effective in capturing variance, the residual plots still indicated potential issues. This suggests that further refinement or alternative models might be necessary to improve prediction accuracy and address residual patterns.

## Conclusion

- **Manual Feature Selection**: Effective in identifying feature combinations that generally resulted in lower RMSE. However, the addition of 'Volume' did not consistently enhance predictive accuracy and sometimes worsened it.
- **PCA**: Successfully reduced the feature set and captured variance but did not fully resolve residual issues, indicating the need for additional model adjustments or alternative approaches.

## Future Work

Further exploration of other models and techniques is recommended to address the residual patterns and improve prediction accuracy.

---

For more details, refer to the code and analysis in the project's repository.
