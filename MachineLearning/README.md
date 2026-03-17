# MachineLearning

This folder contains a comprehensive **machine learning library** implementing a wide range of supervised, unsupervised, and reinforcement learning algorithms.

## Algorithms Included

### Supervised Learning – Classification
- **K-Nearest Neighbors (KNN)** (`KNN.h`): Classifies a sample by majority vote among its k closest neighbors in feature space.
- **Naive Bayes** (`NaiveBayes.h`): A probabilistic classifier based on Bayes' theorem, assuming features are independent.
- **Decision Tree** (`DecisionTree.h`): Learns a tree of if/else rules from training data. Interpretable and fast.
- **Random Forest** (`RandomForest.h`): An ensemble of decision trees trained on random subsets of data and features; more accurate and robust than a single tree.
- **Kernel SVM** (`KernelSVM.h`): Support Vector Machine with kernel functions for non-linear classification.
- **Neural Network** (`NeuralNetwork.h`): Multi-layer perceptron (MLP) with backpropagation; the foundation of deep learning.
- **Cost-Sensitive Classification** (`CostSensitiveClassification.h`): Handles imbalanced classes or asymmetric misclassification costs.

### Supervised Learning – Regression
- **Regression** (`Regression.h`): Linear and logistic regression models.
- **Lasso** (`Lasso.h`): Regularized linear regression (L1 penalty) for feature selection and sparsity.

### Unsupervised Learning
- **Clustering** (`Clustering.h`): Groups similar data points together (e.g., k-means, hierarchical clustering).
- **Association Rules** (`APriori.h`): Discovers frequent itemsets and association rules (e.g., "customers who buy X also buy Y") using the Apriori algorithm.

### Reinforcement Learning
- **Reinforcement Learning** (`ReinforcementLearning.h`): Algorithms for training agents to take actions in an environment to maximize cumulative reward (e.g., Q-learning).

### Data Utilities
- **Dataset Reader** (`ReadClassificationData.h`): Loads classification datasets from files.
- **Datasets/** – Sample classification datasets for testing.
- **RegDatasets/** – Sample regression datasets for testing.

## Files

| File | Description |
|------|-------------|
| `Classification.h` | General classification interface |
| `Regression.h` | Linear and logistic regression |
| `Clustering.h` | Clustering algorithms (k-means, etc.) |
| `DecisionTree.h` | Decision tree classifier |
| `RandomForest.h` | Random forest ensemble |
| `NeuralNetwork.h` | Multi-layer perceptron |
| `KernelSVM.h` | Kernel Support Vector Machine |
| `KNN.h` | K-Nearest Neighbors |
| `NaiveBayes.h` | Naive Bayes classifier |
| `Lasso.h` | Lasso (L1-regularized) regression |
| `APriori.h` | Apriori association rule mining |
| `ReinforcementLearning.h` | Reinforcement learning (Q-learning, etc.) |
| `CostSensitiveClassification.h` | Cost-sensitive and imbalanced classification |
| `ReadClassificationData.h` | Dataset loading utilities |
| `Datasets/` | Sample classification datasets |
| `RegDatasets/` | Sample regression datasets |
| `*TestAuto.h` | Automated test helpers |
| `test*.cpp` | Test drivers |

## Usage

Compile and run the test drivers:

```bash
g++ -O2 -o testML test.cpp && ./testML
```

> **Note:** Test drivers load data from the `Datasets/` and `RegDatasets/` subdirectories. Run tests from the `MachineLearning/` directory.
