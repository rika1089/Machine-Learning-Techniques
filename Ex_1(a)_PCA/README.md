# Exercise 1(a): Principal Component Analysis (PCA)

## Objective
To understand and implement Principal Component Analysis, a fundamental dimensionality reduction technique used in machine learning for feature extraction and data visualization.

## Overview
Principal Component Analysis (PCA) is an unsupervised learning technique that:
- Reduces the number of features while preserving maximum variance
- Identifies principal components (directions of maximum variance)
- Transforms high-dimensional data into a lower-dimensional space
- Helps in data visualization and feature extraction

## Key Concepts

### What is PCA?
- **Dimensionality Reduction**: Reduces the number of features in a dataset
- **Variance Preservation**: Maintains the most important information from the data
- **Linear Transformation**: Applies orthogonal transformation to correlated variables
- **Unsupervised Learning**: Works without labeled target variables

### Applications
- Image compression and recognition
- Gene expression analysis
- Data visualization
- Noise reduction
- Feature extraction for classification tasks

## Implementation Details

### Steps in PCA
1. **Standardization**: Normalize features to have zero mean and unit variance
2. **Covariance Matrix**: Calculate covariance between all feature pairs
3. **Eigenvalues & Eigenvectors**: Compute eigenvalues and corresponding eigenvectors
4. **Sort Components**: Arrange principal components by explained variance
5. **Transform Data**: Project data onto selected principal components

## Files in This Exercise

- `Ex_1(a)_PCA.ipynb` - Jupyter notebook with complete PCA implementation
- `Ex_1(a)_PCA.pdf` - Detailed explanation with theory and results

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand the mathematical foundations of PCA
- ✓ Implement PCA from scratch
- ✓ Interpret explained variance ratios
- ✓ Visualize data in reduced dimensions
- ✓ Apply PCA to real-world datasets

## Practical Insights

### When to Use PCA
- ✓ Feature dimensionality reduction
- ✓ Data visualization in 2D/3D
- ✓ Preprocessing before classification
- ✓ Handling multicollinearity
- ✓ Computational efficiency improvement

### Important Notes
- Always standardize features before applying PCA
- Check explained variance cumulative sum to decide number of components
- PCA assumes linear relationships between features
- Original features lose interpretability in transformed space

## Related Concepts
- Linear Algebra (eigenvalues, eigenvectors)
- Covariance and correlation matrices
- Data standardization and normalization
- Scree plots and elbow method

## Further Reading
- Scikit-learn PCA documentation
- Pattern Recognition and Machine Learning (PRML) by Bishop
- Introduction to Statistical Learning (ISL)

---

**Exercise Type**: Dimensionality Reduction  
**Difficulty Level**: Beginner to Intermediate  
**Prerequisites**: Linear Algebra, Statistics  
**Time to Complete**: 2-3 hours
