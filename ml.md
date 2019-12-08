## Error: Bias v.s. Variance
Error mostly coms from bias: underfitting
Error mostly coms from variance: overfitting

## Feature Crosses
A feature cross is a synthetic feature that encodes nonlinearity in the feature
space by multiplying two or more input features together. Create a new feature
$x_3$ by crossing $x_1$ and $x_2$

$$ x_3 = x_1x_2 $$

### [Crossing One-Hot Vectors](https://developers.google.com/machine-learning/crash-course/feature-crosses/crossing-one-hot-vectors)


## Regularization
### Early stopping
### Penalizing Model Complexity
Empirical risk minimization:
    - aims for low training error
    - minimize: $Loss(Data | Model)$
Structural risk minimization:
    - balancing against complexity
    - minimize: $Loss(Data | Model) + complexity(Model)$

#### $L_2$ regularization (a.k.a ridge)
Complexity(model) = sum of the squares of the weights
- Penalize big weights
- for linear models: prefer flatter slopes
- Bayesian prior:
    - weights should be centered around zero and
    - be normally distributed
$$ Loss(Data | Model) + \lambda(w_1^2 + ... + w_n^2) $$

##### Lambda and learning rate
Strong L2 regularization values tend to drive feature weights closer to 0. Lower
learning rates (with early stopping) often produce the same effect because the
steps away from 0 aren't as large. Consequently, tweaking learning rate and
lambda simultaneously may have confounding effects.

# Logistic Regression
LR for the probability outputs - this is a regression in (0, 1)

# Classification
## Evaluation Metrics
True positives/ False positives/ False Negatives/ True Negative
### Accuracy
- Can be misleading
    - classes imbalance
### Precision
### Recall

### ROC Curve
Each point is the TP and FP at one decision threshold.
### AUC
Area under the ROC Curve
### Prediction Bias
