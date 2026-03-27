# Exercise 2: K-Nearest Neighbors (KNN) Classification

## Objective
To understand and implement the K-Nearest Neighbors algorithm, a fundamental non-parametric machine learning algorithm for classification and regression tasks.

## Overview
K-Nearest Neighbors (KNN) is a simple yet powerful algorithm that:
- Makes predictions based on similarity to nearby training examples
- Works well for both classification and regression tasks
- Is a lazy learner (stores all training data)
- Requires no explicit training phase
- Provides intuitive decision boundaries

## Algorithm Fundamentals

### How KNN Works
1. **Store Training Data**: Keep all training examples in memory
2. **Calculate Distance**: Compute distance from query point to all training points
3. **Find Neighbors**: Identify K nearest neighbors based on distance metric
4. **Aggregate**: For classification - majority vote; for regression - average
5. **Predict**: Assign class/value based on neighbors' labels

### Distance Metrics
- **Euclidean Distance**: Standard distance measure in Euclidean space
- **Manhattan Distance**: Sum of absolute differences (L1 norm)
- **Minkowski Distance**: Generalization of Euclidean and Manhattan
- **Hamming Distance**: For categorical features

### Key Parameters
- **K**: Number of neighbors to consider (critical hyperparameter)
- **Distance Metric**: How to measure similarity
- **Weights**: Uniform vs. distance-weighted voting
- **Algorithm**: Brute force, KD-Tree, or Ball-Tree for efficiency

## Advantages and Disadvantages

### Advantages
- ✓ Simple to understand and implement
- ✓ No training phase required
- ✓ Adapts well to complex decision boundaries
- ✓ Works for both classification and regression
- ✓ No assumptions about data distribution

### Disadvantages
- ✗ Slow at prediction time (computes distances to all points)
- ✗ Memory intensive (stores all training data)
- ✗ Sensitive to irrelevant features
- ✗ Sensitive to feature scaling
- ✗ Curse of dimensionality

## Practical Implementation

### Data Preprocessing Requirements
- **Feature Scaling**: Essential (standardization or normalization)
- **Feature Selection**: Remove irrelevant features
- **Missing Values**: Handle before applying KNN
- **Categorical Encoding**: Convert to numerical values

### Hyperparameter Tuning
- **K Selection**: Use cross-validation to find optimal K
- **Distance Metric**: Test different metrics on validation set
- **Weight Scheme**: Compare uniform vs. distance-weighted
- **Algorithm**: Choose based on dimensionality and dataset size

## KNN Variations

### Weighted KNN
- Closer neighbors have more influence
- Weight inversely proportional to distance
- Reduces impact of distant neighbors

### KNN Regression
- Predicts continuous values
- Averages target values of K neighbors
- Can use weighted averaging

### Approximate KNN
- Locality Sensitive Hashing (LSH)
- Reduces computational complexity
- Useful for large datasets

## Files in This Exercise

- `Ex_2_KNN.ipynb` - Jupyter notebook with KNN implementation
- `Ex_2_KNN.pdf` - Detailed explanation and results analysis

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand KNN algorithm mechanics
- ✓ Implement KNN from scratch and using libraries
- ✓ Evaluate KNN classifier performance
- ✓ Tune hyperparameter K effectively
- ✓ Understand KNN strengths and limitations
- ✓ Apply KNN to real-world datasets

## Practical Tips

### For Effective KNN Usage
- **Scale Your Features**: Always normalize/standardize features
- **Try Multiple K Values**: Range from 1 to sqrt(n) samples
- **Use Cross-Validation**: Get reliable performance estimates
- **Handle Imbalanced Data**: Consider class weights if necessary
- **Feature Engineering**: Remove noise and irrelevant features

### Common Pitfalls
- ✗ Forgetting to scale features
- ✗ Using K=1 without validation
- ✗ Not removing outliers
- ✗ High-dimensional data without dimensionality reduction
- ✗ Ignoring computational cost for large datasets

## Performance Considerations

### Time Complexity
- **Training**: O(1) - just stores data
- **Prediction**: O(n*d) - n samples, d dimensions
- **With optimization**: O(log n) using KD-trees

### Space Complexity
- O(n*d) - must store all training data

## Related Algorithms
- **k-Means Clustering**: Uses distance concept
- **KD-Trees**: Efficient neighbor searching
- **Locality Sensitive Hashing**: Approximate neighbor search
- **Distance Metric Learning**: Optimize distance measures

## Further Reading
- Scikit-learn KNN documentation
- "The Elements of Statistical Learning" - Hastie, Tibshirani, Friedman
- KNN optimization techniques and variants

---

**Exercise Type**: Supervised Learning - Classification  
**Difficulty Level**: Beginner  
**Prerequisites**: Python, Linear Algebra, Distance Metrics  
**Time to Complete**: 2-3 hours
