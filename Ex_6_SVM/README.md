# Exercise 6: Support Vector Machine (SVM)

## Objective
To understand and implement Support Vector Machines, a powerful supervised learning algorithm for classification and regression that finds optimal hyperplanes to maximize the margin between classes.

## Overview
Support Vector Machines are:
- Binary and multiclass classifiers
- Effective in high-dimensional spaces
- Memory efficient using support vectors
- Versatile with various kernel functions
- Excellent for both linear and non-linear problems

## SVM Fundamentals

### Basic Concept
- Finds optimal hyperplane maximizing margin between classes
- Margin = distance from hyperplane to nearest points
- Support vectors = critical points closest to hyperplane
- Only support vectors matter for decision boundary

### Mathematical Formulation
- **Objective**: Minimize ||w||²/2 + C*Σ(ξi)
- **Constraint**: yi(w·xi + b) ≥ 1 - ξi
- **w** = weight vector, **b** = bias
- **ξ** = slack variables (handle misclassification)
- **C** = regularization parameter

## Key Concepts

### Margin
- **Hard Margin**: Perfect separation (no misclassification)
- **Soft Margin**: Allows some misclassification
- **Regularization**: Trade-off between margin and errors

### Kernel Functions
- **Linear**: w·x + b (linear problems)
- **Polynomial**: (γ·x·y + r)^d (polynomial boundaries)
- **RBF**: exp(-γ||x-y||²) (most versatile)
- **Sigmoid**: tanh(γ·x·y + r) (neural-like)

## Advantages and Disadvantages

### Advantages
- ✓ Effective in high dimensions
- ✓ Memory efficient (uses support vectors)
- ✓ Versatile kernel functions
- ✓ Good generalization
- ✓ Works with non-linear data
- ✓ Clear mathematical foundation

### Disadvantages
- ✗ Slow for large datasets
- ✗ Hard to interpret decision boundaries
- ✗ Sensitive to feature scaling
- ✗ Hyperparameter tuning needed
- ✗ Quadratic programming complexity

## SVM Types

### SVC (Support Vector Classification)
- Binary and multiclass classification
- One-vs-one or One-vs-rest strategies
- Probability calibration available

### SVR (Support Vector Regression)
- Predicts continuous values
- Similar principle to SVC
- Epsilon-insensitive loss

## Hyperparameters

### C Parameter
- Controls regularization strength
- High C: less regularization, may overfit
- Low C: more regularization, may underfit
- Range: 0.001 to 1000

### Kernel and Parameters
- **Linear**: No additional parameters
- **Polynomial**: degree, gamma, coef0
- **RBF**: gamma (kernel coefficient)
- **Sigmoid**: gamma, coef0

### Gamma Parameter (for RBF)
- Controls kernel influence
- High gamma: tight fit, may overfit
- Low gamma: loose fit, may underfit
- Auto: 1/n_features

## Implementation Considerations

### Feature Scaling
- Essential for SVM performance
- Use StandardScaler or MinMaxScaler
- Scale both training and test data

### Class Imbalance
- Use class weights (class_weight='balanced')
- Adjust C inversely to class frequency
- Consider resampling

### Optimization Algorithms
- **Sequential Minimal Optimization (SMO)**: Scikit-learn default
- **Stochastic Gradient Descent (SGD)**: For large datasets

## Mathematical Insights

### Decision Function
- f(x) = w·φ(x) + b = Σ αi*yi*K(xi,x) + b
- K(xi,x) = kernel function
- αi = Lagrange multipliers (only non-zero for support vectors)

### Kernel Trick
- Enables non-linear classification in higher dimensions
- Avoids explicit transformation
- Computational efficiency

## Files in This Exercise

- `Ex_6_SVM.ipynb` - Jupyter notebook with implementation
- `Ex_6_SVM.pdf` - Analysis and results

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand SVM mathematical foundations
- ✓ Implement SVM from scratch
- ✓ Apply different kernel functions
- ✓ Tune hyperparameters effectively
- ✓ Handle non-linear classification
- ✓ Evaluate SVM models properly

## Common Issues and Solutions

### Slow Training
- **Solution**: Use SGDClassifier for large datasets
- **Solution**: Reduce feature dimensionality
- **Solution**: Use simpler kernels (linear)

### Poor Performance
- **Solution**: Scale features properly
- **Solution**: Tune C and kernel parameters
- **Solution**: Try different kernels
- **Solution**: Handle class imbalance

### Overfitting
- **Solution**: Increase regularization (decrease C)
- **Solution**: Simplify kernel (try linear)
- **Solution**: Reduce features

## Comparison with Other Classifiers

| Aspect | SVM | Logistic Regression | Neural Networks |
|--------|-----|-------------------|------------------|
| Non-linearity | Kernel trick | No (linear) | Yes (inherent) |
| Training Speed | Slow | Fast | Medium |
| Memory | Efficient | Efficient | Heavy |
| Interpretability | Low | High | Very Low |
| Large Data | Not ideal | Ideal | Good |

## Further Reading
- "Support Vector Machines" by Smola & Schölkopf
- "Learning with Kernels" by Schölkopf & Smola
- Scikit-learn SVM documentation

---

**Exercise Type**: Supervised Learning - Classification/Regression  
**Difficulty Level**: Intermediate to Advanced  
**Prerequisites**: Linear Algebra, Optimization, Kernel Methods  
**Time to Complete**: 3-4 hours
