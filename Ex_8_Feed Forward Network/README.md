# Exercise 8: Feed Forward Neural Networks

## Objective
To understand and implement Feed Forward Neural Networks (FFNNs), the foundational deep learning architecture used for classification and regression tasks.

## Overview
Feed Forward Neural Networks:
- Fundamental architecture for deep learning
- Consists of input, hidden, and output layers
- Universal approximators for continuous functions
- Trained using backpropagation algorithm
- Highly flexible and powerful for complex problems

## Neural Network Fundamentals

### Architecture Components
1. **Input Layer**: Receives raw features
2. **Hidden Layers**: Learn representations (1 to many layers)
3. **Output Layer**: Produces predictions
4. **Neurons**: Perform weighted sum + activation
5. **Weights & Biases**: Learnable parameters

### Forward Pass
- Input flows through network layers
- Each neuron: output = activation(w*x + b)
- Information propagates from input to output
- Final layer determines prediction

### Activation Functions
- **ReLU**: Rectified Linear Unit (most common, hidden layers)
- **Sigmoid**: S-shaped (binary classification output)
- **Tanh**: Hyperbolic tangent (hidden layers)
- **Softmax**: Multi-class classification output
- **Linear**: Regression tasks

## Network Architecture Design

### Shallow vs Deep Networks
- **Shallow**: 1-2 hidden layers (simple problems)
- **Deep**: 3+ hidden layers (complex problems)
- **Trade-off**: More layers = more capacity, harder to train

### Layer Sizes
- **Input Layer**: Number of features
- **Hidden Layers**: 2x-8x input size (heuristic)
- **Output Layer**: Number of classes/outputs
- Start simple, increase complexity if needed

### Hyperparameters
- **Learning Rate**: Controls update step size (0.001-0.1 typical)
- **Batch Size**: Number of samples per update (32-256 common)
- **Epochs**: Number of passes through data
- **Optimizer**: Adam, SGD, RMSprop, etc.
- **Loss Function**: MSE (regression), Cross-entropy (classification)

## Training Process

### Backpropagation Algorithm
1. **Forward Pass**: Compute predictions
2. **Compute Loss**: Measure prediction error
3. **Backward Pass**: Calculate gradients via chain rule
4. **Update Parameters**: Adjust weights using gradients
5. **Repeat**: Process for multiple epochs

### Optimization Techniques
- **Gradient Descent**: Basic optimization
- **Adam**: Adaptive learning rates (most popular)
- **RMSprop**: Root Mean Square Propagation
- **Momentum**: Accelerates convergence
- **Learning Rate Scheduling**: Decay over time

## Regularization Techniques

### Prevent Overfitting
- **L1/L2 Regularization**: Penalty on weights
- **Dropout**: Randomly disable neurons during training
- **Early Stopping**: Stop when validation loss plateaus
- **Batch Normalization**: Normalize layer inputs
- **Data Augmentation**: Generate more training data

## Advantages and Disadvantages

### Advantages
- ✓ Universal approximators
- ✓ Handle complex non-linear relationships
- ✓ Learn hierarchical representations
- ✓ Can handle diverse data types
- ✓ Scalable with GPU acceleration

### Disadvantages
- ✗ Requires large datasets
- ✗ Computationally expensive to train
- ✗ Hard to interpret (black box)
- ✗ Hyperparameter tuning critical
- ✗ Prone to overfitting

## Implementation Frameworks

### Popular Libraries
- **TensorFlow/Keras**: High-level API, flexible
- **PyTorch**: Dynamic computation graphs, research-friendly
- **Scikit-learn MLPClassifier**: Simple FFNNs
- **Theano, Caffe**: Legacy frameworks

## Practical Workflow

### Step-by-Step Training
1. **Data Preparation**: Normalize, split into train/test
2. **Model Definition**: Define architecture
3. **Compilation**: Specify optimizer and loss
4. **Training**: Fit model on training data
5. **Evaluation**: Assess on test/validation data
6. **Tuning**: Adjust hyperparameters if needed
7. **Deployment**: Use trained model for predictions

## Common Issues and Solutions

### Vanishing Gradients
- **Cause**: Gradients become very small in deep networks
- **Solution**: Use ReLU, batch normalization, residual connections

### Exploding Gradients
- **Cause**: Gradients become very large
- **Solution**: Gradient clipping, normalize inputs

### Overfitting
- **Cause**: Model too complex for data
- **Solution**: Dropout, L2 regularization, early stopping

### Underfitting
- **Cause**: Model too simple
- **Solution**: Add layers, increase capacity, train longer

## Files in This Exercise

- `Ex_8_Feed Forward Network.ipynb` - Implementation with Keras/TensorFlow
- `Ex_8_Feed Forward Network.pdf` - Analysis and visualizations

## Learning Outcomes

After completing this exercise, you will:
- ✓ Understand FFNN architecture and theory
- ✓ Implement networks with Keras/TensorFlow
- ✓ Design appropriate network architectures
- ✓ Train and validate neural networks
- ✓ Apply regularization techniques
- ✓ Troubleshoot common training issues
- ✓ Achieve competitive performance on classification/regression

## Best Practices

### For Effective Training
1. **Start Simple**: Begin with simple architecture
2. **Monitor Training**: Track loss and accuracy curves
3. **Use Validation Set**: Detect overfitting early
4. **Normalize Features**: Standardize input data
5. **Batch Normalization**: Improves convergence
6. **Early Stopping**: Prevent unnecessary training

### Hyperparameter Tuning Tips
- Start with learning rate = 0.001
- Use Adam optimizer by default
- Set batch size = 32 or 64
- Monitor validation loss for early stopping
- Use callbacks for flexible control

## Advanced Topics
- Convolutional Neural Networks (CNNs)
- Recurrent Neural Networks (RNNs)
- Transfer Learning
- Attention Mechanisms
- Transformer Architectures

## Further Reading
- "Deep Learning" by Goodfellow, Bengio, Courville
- Keras documentation
- PyTorch tutorials
- Research papers on specific architectures

---

**Exercise Type**: Deep Learning - Neural Networks  
**Difficulty Level**: Intermediate to Advanced  
**Prerequisites**: Linear Algebra, Calculus, Backpropagation  
**Time to Complete**: 4-5 hours
