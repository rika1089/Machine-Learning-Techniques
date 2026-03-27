# Exercise 7: Support Vector Machine with Varying Kernels

## Objective
To explore and compare different SVM kernel functions and understand how kernel selection impacts classification performance on real-world datasets.

## Overview
This exercise focuses on:
- Understanding kernel functions fundamentally
- Comparing Linear, Polynomial, RBF, and Sigmoid kernels
- Effect of kernel parameters on decision boundaries
- Performance trade-offs across different kernels
- Practical kernel selection strategies

## Kernel Functions Detailed

### 1. Linear Kernel
**Formula**: K(x, y) = x · y
- **Best for**: Linearly separable data
- **Advantage**: Fast computation, interpretable
- **Disadvantage**: Limited to linear boundaries
- **Use case**: High-dimensional text data
- **Parameters**: None

### 2. Polynomial Kernel
**Formula**: K(x, y) = (γ·x·y + r)^d
- **Best for**: Polynomial decision boundaries
- **Parameters**:
  - **d (degree)**: Polynomial degree (1-5 typical)
  - **γ (gamma)**: Kernel coefficient
  - **r (coef0)**: Independent term
- **Advantage**: Flexible, captures feature interactions
- **Disadvantage**: Computational cost, more parameters
- **Use case**: Medium-complexity non-linear problems

### 3. RBF (Radial Basis Function) Kernel
**Formula**: K(x, y) = exp(-γ||x-y||²)
- **Best for**: Most non-linear problems
- **Most Popular**: Default choice for many practitioners
- **Parameters**:
  - **γ (gamma)**: Reaches of influence of single training point
  - Small γ: far reach, simple model
  - Large γ: local reach, complex model
- **Advantage**: Very flexible, handles complex data
- **Disadvantage**: Sensitive to parameter tuning
- **Use case**: General non-linear classification

### 4. Sigmoid Kernel
**Formula**: K(x, y) = tanh(γ·x·y + r)
- **Best for**: Neural network-like behavior
- **Parameters**: γ, r (similar to polynomial)
- **Advantage**: Neural network-like behavior
- **Disadvantage**: Less commonly used, requires careful tuning
- **Use case**: Specific neural-inspired applications

## Kernel Selection Guide

### Decision Flow
1. **Linear Separable Data** → Linear Kernel
2. **Small to Medium Dataset** → RBF or Polynomial
3. **High Dimensional Data** → Linear Kernel
4. **Unknown Complexity** → Try RBF first
5. **Need Interpretability** → Linear Kernel

### Performance Factors
- **Dataset Size**: Linear for large, RBF for small-medium
- **Feature Dimension**: Linear for high-d, RBF for low-d
- **Data Complexity**: Linear (simple) to RBF (complex)
- **Computational Budget**: Linear < Polynomial < RBF

## Parameter Tuning

### Gamma (γ) Effects
- **Low γ**: Smooth decision boundaries, may underfit
- **High γ**: Complex boundaries, may overfit
- **Auto**: 1/(n_features)
- **Range**: Typically 0.0001 to 100 (logarithmic scale)

### Degree (d) for Polynomial
- **1**: Linear
- **2**: Quadratic (parabolas)
- **3**: Cubic (more complex curves)
- **4-5**: Very complex (rarely needed)

### C Parameter (independent of kernel)
- Controls regularization
- Affects all kernels similarly
- Range: 0.001 to 1000

## Practical Comparison

### Computational Complexity
| Kernel | Training | Prediction | Memory |
|--------|----------|-----------|--------|
| Linear | O(n) | O(d) | O(m) |
| Polynomial | O(n²) | O(m*d) | O(m) |
| RBF | O(n²) | O(m*d) | O(m) |
| Sigmoid | O(n²) | O(m*d) | O(m) |

### Accuracy vs Speed Trade-off
- **Fastest**: Linear
- **Balanced**: Polynomial (low degree)
- **Slowest**: RBF, Sigmoid
- **Most Accurate**: Usually RBF (with proper tuning)

## Visualization and Analysis

### Decision Boundaries
- Linear: Straight lines/hyperplanes
- Polynomial: Curved boundaries
- RBF: Highly flexible, localized boundaries
- Sigmoid: Neural network-like curves

### Support Vector Distribution
- Different kernels create different support vector sets
- RBF often uses more support vectors
- Linear uses fewer support vectors

## Files in This Exercise

- `Ex_7_SVM(Varying kernels).ipynb` - Kernel comparison implementation
- `Ex_7_SVM(Varying kernels).pdf` - Analysis and visualizations

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand mathematical formulations of kernel functions
- ✓ Compare kernel performance empirically
- ✓ Visualize decision boundaries for different kernels
- ✓ Tune kernel-specific parameters
- ✓ Select appropriate kernels for different problems
- ✓ Understand kernel computation costs

## Best Practices

### Kernel Selection Strategy
1. Start with linear kernel (quick baseline)
2. If linear fails, try RBF
3. Use polynomial for specific requirements
4. Avoid sigmoid unless domain-specific
5. Always scale features before SVM

### Hyperparameter Tuning
- Use GridSearchCV or RandomizedSearchCV
- Test C range: [0.1, 1, 10, 100]
- Test γ range: [1e-4, 1e-3, 1e-2, 0.1, 1]
- Use cross-validation for reliable estimates

## Common Issues

### Poor RBF Performance
- **Cause**: Features not scaled
- **Solution**: Use StandardScaler before SVM

### All Kernels Perform Poorly
- **Cause**: Feature quality issues
- **Solution**: Feature engineering/selection

### Overfitting with Complex Kernels
- **Cause**: High γ or high degree
- **Solution**: Increase C, reduce γ/degree

## Further Reading
- SVM kernel theory papers
- Kernel method tutorials
- Scikit-learn kernel documentation

---

**Exercise Type**: Kernel Methods - Classification  
**Difficulty Level**: Intermediate to Advanced  
**Prerequisites**: SVM fundamentals, Linear Algebra  
**Time to Complete**: 3-4 hours
