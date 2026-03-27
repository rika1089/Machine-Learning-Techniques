# Exercise 4: Linear Regression

## Objective
To understand and implement Linear Regression, a fundamental supervised learning algorithm for predicting continuous values using linear relationships between input features and target variables.

## Overview
Linear Regression is a statistical method that:
- Models linear relationships between features and target
- Predicts continuous numerical values
- Assumes linear association between variables
- Uses least squares method for optimization
- Provides interpretable model coefficients

## Regression Fundamentals

### How Linear Regression Works
1. **Assume Linear Relationship**: y = β0 + β1*x1 + β2*x2 + ... + βn*xn
2. **Minimize Error**: Minimize sum of squared residuals (RSS)
3. **Calculate Parameters**: Solve using closed-form solution or gradient descent
4. **Make Predictions**: Use learned parameters to predict new values
5. **Evaluate Model**: Assess performance using appropriate metrics

### Simple vs Multiple Regression
- **Simple Regression**: Single input feature
- **Multiple Regression**: Multiple input features
- **Polynomial Regression**: Non-linear relationships using polynomial terms

## Key Concepts

### Loss Function
- **Mean Squared Error (MSE)**: Average of squared differences
- **Residuals**: Differences between actual and predicted values
- **Least Squares**: Minimizes sum of squared residuals

### Assumptions in Linear Regression
1. **Linearity**: Linear relationship between X and y
2. **Independence**: Observations are independent
3. **Homoscedasticity**: Constant variance of errors
4. **Normality**: Errors are normally distributed
5. **No Multicollinearity**: Features not highly correlated

## Regression vs Classification

| Aspect | Regression | Classification |
|--------|-----------|----------------|
| Target | Continuous values | Discrete classes |
| Output | Real numbers | Class labels |
| Loss Function | MSE, MAE | Cross-entropy, Hinge |
| Metrics | R², RMSE, MAE | Accuracy, Precision, Recall |
| Activation | Linear | Sigmoid, Softmax |

## Implementation Approaches

### Normal Equation (Closed-form)
- β = (XTX)^(-1) XTy
- Direct calculation of optimal parameters
- Fast for small datasets
- Computationally expensive for large datasets (O(n³))

### Gradient Descent
- Iterative optimization approach
- Updates parameters in direction of steepest descent
- Scalable to large datasets
- Requires learning rate tuning
- Multiple variants: Batch, Stochastic, Mini-batch

## Regression Variants

### Ridge Regression (L2 Regularization)
- Adds penalty for large coefficients
- Prevents overfitting
- Shrinks coefficients but doesn't eliminate them
- Controlled by alpha parameter

### Lasso Regression (L1 Regularization)
- Can shrink some coefficients to exactly zero
- Performs feature selection
- More interpretable models
- Sparse solutions

### Elastic Net
- Combines L1 and L2 regularization
- Balances benefits of Ridge and Lasso
- Two hyperparameters to tune

## Model Evaluation Metrics

### Regression Metrics
- **R-squared (R²)**: Proportion of variance explained (0-1)
- **Adjusted R²**: Accounts for number of features
- **RMSE**: Root Mean Squared Error (same scale as y)
- **MAE**: Mean Absolute Error (robust to outliers)
- **MAPE**: Mean Absolute Percentage Error

## Practical Implementation

### Data Preparation
- Handle missing values appropriately
- Standardize/normalize features for gradient descent
- Detect and handle outliers
- Engineer meaningful features
- Check for multicollinearity (VIF > 10)

### Feature Selection
- Remove highly correlated features
- Use domain knowledge
- Stepwise selection methods
- Regularization-based selection

## Advantages and Disadvantages

### Advantages
- ✓ Simple and interpretable
- ✓ Fast to train
- ✓ Works well for linear relationships
- ✓ Provides feature importance (coefficients)
- ✓ Strong statistical foundation

### Disadvantages
- ✗ Assumes linearity
- ✗ Sensitive to outliers
- ✗ Requires careful feature engineering
- ✗ Poor performance with non-linear data
- ✗ Multicollinearity issues

## Files in This Exercise

- `Ex_4_Linear_Regression.ipynb` - Jupyter notebook with implementation
- `Ex_4_Linear_Regression.pdf` - Analysis and results

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand linear regression mathematics
- ✓ Implement regression from scratch
- ✓ Use scikit-learn regression models
- ✓ Evaluate regression models effectively
- ✓ Apply regularization techniques
- ✓ Interpret model coefficients
- ✓ Handle real-world regression problems

## Common Issues and Solutions

### Overfitting
- **Solution**: Use regularization (Ridge/Lasso/Elastic Net)
- **Solution**: Reduce model complexity
- **Solution**: Increase training data

### Underfitting
- **Solution**: Add more features
- **Solution**: Reduce regularization strength
- **Solution**: Try polynomial features

### Multicollinearity
- **Solution**: Remove correlated features
- **Solution**: Use PCA for dimensionality reduction
- **Solution**: Use Ridge or Elastic Net regression

## Mathematical Formula

### Linear Regression Equation
- **Prediction**: ŷ = β0 + β1*x1 + β2*x2 + ... + βn*xn
- **MSE**: (1/m) * Σ(yi - ŷi)²
- **RMSE**: √MSE

## Related Techniques
- Polynomial Regression
- Ridge & Lasso Regression
- Elastic Net
- Principal Component Regression
- Logistic Regression (for classification)

## Further Reading
- "The Elements of Statistical Learning" by Hastie et al.
- "Applied Linear Regression" by Weisberg
- Scikit-learn regression documentation

---

**Exercise Type**: Supervised Learning - Regression  
**Difficulty Level**: Beginner  
**Prerequisites**: Linear Algebra, Statistics, Calculus  
**Time to Complete**: 2-3 hours
