# Exercise 3: Linear Discriminant Analysis (LDA)

## Objective
To understand and implement Linear Discriminant Analysis, a supervised dimensionality reduction and classification technique that finds linear combinations of features that best separate classes.

## Overview
Linear Discriminant Analysis (LDA) is a statistical technique that:
- Finds linear combinations of features that separate classes
- Reduces dimensionality while maintaining class separability
- Works as both dimensionality reduction and classifier
- Assumes Gaussian distribution of classes
- Assumes equal covariance matrices across classes

## LDA Fundamentals

### How LDA Works
1. **Calculate Mean Vectors**: Compute mean for each class
2. **Within-Class Scatter**: Calculate scatter of points within each class
3. **Between-Class Scatter**: Calculate scatter between class means
4. **Maximize Ratio**: Find projections that maximize between-class scatter / within-class scatter
5. **Select Components**: Choose top discriminative components

### Key Concepts
- **Fisher Criterion**: Maximizes separability between classes
- **Scatter Matrices**: Within-class and between-class scatter
- **Eigenvectors**: Represent discriminative directions
- **Transformation**: Project data into lower-dimensional space

## LDA vs PCA

### Key Differences
| Aspect | LDA | PCA |
|--------|-----|-----|
| Type | Supervised | Unsupervised |
| Objective | Maximize class separation | Maximize variance |
| Uses | Class labels | Ignored |
| Output | Discriminative features | Maximum variance |
| Components | At most C-1 (C = classes) | Up to min(n,d) |

## Assumptions in LDA

### Important Assumptions
- Gaussian distribution of features within each class
- Equal covariance matrices across classes
- Linear decision boundaries
- Homoscedasticity (equal variance in all dimensions)

### When Assumptions are Violated
- Quadratic Discriminant Analysis (QDA) for different covariances
- Non-linear methods for non-linear boundaries
- Data transformation to improve normality

## Practical Implementation

### Data Preparation
- Ensure sufficient samples per class
- Handle class imbalance if present
- Remove outliers and noisy data
- Standardize features (important for LDA)

### LDA Applications
- Face recognition and biometrics
- Medical diagnosis classification
- Credit risk assessment
- Document classification
- Gene expression analysis

## Advantages and Disadvantages

### Advantages
- ✓ Efficient computation
- ✓ No parameter tuning needed
- ✓ Interpretable results
- ✓ Handles multiclass problems well
- ✓ Reduces overfitting through dimensionality reduction

### Disadvantages
- ✗ Assumes Gaussian distribution
- ✗ Assumes equal covariance matrices
- ✗ Limited to linear decision boundaries
- ✗ Sensitive to outliers
- ✗ May fail with small sample sizes

## LDA Variants

### Quadratic Discriminant Analysis (QDA)
- Relaxes equal covariance assumption
- Each class has own covariance matrix
- More flexible but requires more parameters

### Regularized LDA
- Adds regularization term
- Better handles small sample sizes
- Improves numerical stability

### Flexible Discriminant Analysis (FDA)
- Allows non-linear feature transformations
- Uses smoothing splines
- More complex but handles non-linearity

## Files in This Exercise

- `Ex_3_LDA.ipynb` - Jupyter notebook with LDA implementation
- `Ex_3_LDA.pdf` - Detailed explanation and classification results

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand LDA mathematical foundations
- ✓ Implement LDA from scratch
- ✓ Apply LDA for dimensionality reduction
- ✓ Use LDA for multiclass classification
- ✓ Compare LDA with PCA and other methods
- ✓ Interpret discriminative features

## Practical Considerations

### For Effective LDA Usage
- Check Gaussian assumption with Q-Q plots
- Test equal covariance with Box's M test
- Use with balanced datasets when possible
- Always standardize features
- Visualize results in reduced space

### Common Issues and Solutions
- **Singular Covariance**: Use regularization or remove correlated features
- **Overfitting**: Reduce number of features or increase regularization
- **Class Imbalance**: Use class weights or resampling techniques
- **Non-linear Data**: Consider QDA or kernel methods

## Mathematics Summary

### Scatter Matrices
- **Within-class scatter**: Sw = Σ(Xi - mi)(Xi - mi)T
- **Between-class scatter**: Sb = Σ ni(mi - m)(mi - m)T

### Fisher Criterion
- Maximize: J = det(Sb) / det(Sw)
- Solution: Eigenvectors of Sw-1 * Sb

## Related Techniques
- Principal Component Analysis (PCA)
- Quadratic Discriminant Analysis (QDA)
- Logistic Regression
- Support Vector Machines
- Neural Networks

## Further Reading
- "The Elements of Statistical Learning" by Hastie et al.
- "Pattern Recognition and Machine Learning" by Bishop
- Scikit-learn LDA documentation

---

**Exercise Type**: Supervised Learning - Classification & Dimensionality Reduction  
**Difficulty Level**: Intermediate  
**Prerequisites**: Linear Algebra, Statistics, Probability  
**Time to Complete**: 2-3 hours
