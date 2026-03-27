# Exercise 5: Naive Bayes Classification

## Objective
To understand and implement Naive Bayes, a probabilistic classification algorithm based on Bayes' theorem that assumes feature independence and is particularly effective for text classification and categorical data.

## Overview
Naive Bayes is a probabilistic classifier that:
- Uses Bayes' theorem for probability calculation
- Assumes conditional independence of features (naive assumption)
- Works well despite strong independence assumption
- Fast and efficient for training and prediction
- Performs surprisingly well on many real-world problems

## Bayes' Theorem Fundamentals

### Formula
P(C|X) = P(X|C) * P(C) / P(X)

Where:
- **P(C|X)**: Posterior probability (what we want to predict)
- **P(X|C)**: Likelihood (probability of X given class C)
- **P(C)**: Prior probability (probability of class C)
- **P(X)**: Evidence (probability of X)

### Naive Independence Assumption
- Features are conditionally independent given the class
- P(X1,X2,...,Xn|C) = P(X1|C) * P(X2|C) * ... * P(Xn|C)
- Simplifies computation significantly
- Rarely true in practice but works well empirically

## Naive Bayes Variants

### Gaussian Naive Bayes
- Assumes continuous features follow Gaussian distribution
- Best for numerical features
- Suitable for continuous data

### Multinomial Naive Bayes
- Designed for discrete count data
- Commonly used for text classification (word counts)
- Used with bag-of-words representation

### Bernoulli Naive Bayes
- For binary/boolean features
- Features are binary (present/absent)
- Also used in text classification (presence/absence of words)

## How Naive Bayes Works

### Training Phase
1. Calculate prior probability P(C) for each class
2. Calculate conditional probabilities P(Xi|C) for each feature
3. Store these probabilities for prediction

### Prediction Phase
1. Calculate posterior probability for each class
2. Select class with highest posterior probability
3. Apply log probabilities to avoid numerical underflow

## Advantages and Disadvantages

### Advantages
- ✓ Fast and efficient training and prediction
- ✓ Works well with high-dimensional data
- ✓ Requires small training dataset
- ✓ Effective for text classification
- ✓ Probabilistic predictions (confidence scores)
- ✓ Handles categorical and numerical features

### Disadvantages
- ✗ Strong independence assumption (rarely true)
- ✗ Zero probability problem (requires smoothing)
- ✗ Biased probability estimates
- ✗ May underperform with correlated features
- ✗ Assumes feature independence

## Practical Applications

### Text Classification
- Spam detection
- Sentiment analysis
- Topic categorization
- Document classification

### Other Applications
- Email filtering
- Medical diagnosis
- Credit risk assessment
- Real-time prediction

## Implementation Considerations

### Smoothing Techniques
- **Laplace Smoothing**: Add 1 to avoid zero probabilities
- **Lidstone Smoothing**: Add alpha value for smoothing
- **No Smoothing**: Skip if zero probabilities unlikely

### Feature Preprocessing
- Feature scaling not necessary (probabilistic approach)
- Handle missing values appropriately
- Categorical encoding if needed
- Feature selection improves performance

### Hyperparameters
- **Alpha**: Smoothing parameter (typically 1.0 for Laplace)
- **Class Prior**: Can be adjusted for imbalanced classes
- **Feature Type**: Gaussian, Multinomial, or Bernoulli

## Mathematical Formulation

### Classification Decision
- ŷ = argmax(C) P(C) * ∏ P(Xi|C)
- Using log: ŷ = argmax(C) log(P(C)) + Σ log(P(Xi|C))

### Probability Estimates
- P(Xi|C) = (count(Xi,C) + alpha) / (count(C) + alpha*n_features)
- P(C) = count(C) / total_samples

## Handling Data Issues

### Zero Probability Problem
- Use Laplace smoothing (add 1)
- Use Lidstone smoothing (add alpha)
- Prevents zero probabilities in multiplication

### Class Imbalance
- Use class weights during training
- Adjust prior probabilities
- Consider resampling techniques

## Files in This Exercise

- `Ex_5_Naive_Bayes.ipynb` - Jupyter notebook with implementation
- `Ex_5_Naive_Bayes.pdf` - Analysis and results

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand Bayes' theorem and its application
- ✓ Implement Naive Bayes from scratch
- ✓ Apply different Naive Bayes variants
- ✓ Handle text classification tasks
- ✓ Apply smoothing techniques
- ✓ Evaluate probabilistic classifiers

## Common Pitfalls

### Avoiding Mistakes
- ✗ Not applying smoothing (zero probability issue)
- ✗ Ignoring feature dependence issues
- ✗ Using on highly correlated feature sets
- ✗ Not preprocessing text data properly
- ✗ Overlooking class imbalance

### Solutions
- Use appropriate smoothing
- Feature selection to reduce dependence
- Preprocessing and normalization
- Handle class imbalance with weights
- Cross-validation for reliable estimates

## Comparison with Other Classifiers

| Aspect | Naive Bayes | Logistic Regression | SVM |
|--------|-------------|-------------------|-----|
| Speed | Fast | Medium | Slow |
| Scalability | High | High | Medium |
| Feature Space | Any | Continuous | Any |
| Probabilistic | Yes | Yes | No |
| Interpretable | Yes | Yes | No |

## Further Reading
- "Machine Learning" by Tom Mitchell
- Scikit-learn Naive Bayes documentation
- Text classification papers

---

**Exercise Type**: Supervised Learning - Classification  
**Difficulty Level**: Beginner  
**Prerequisites**: Probability, Statistics, Bayes' Theorem  
**Time to Complete**: 2-3 hours
