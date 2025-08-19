# Implementing the Perceptron Learning Algorithm (PLA) for Binary Classification

## 1. Introduction

This project demonstrates the implementation of the Perceptron Learning Algorithm (PLA) from scratch in Python. The perceptron is one of the earliest supervised learning algorithms used for binary classification. The objective is to understand how the perceptron works, observe its convergence behavior on linearly separable data, and highlight its limitations on non-linearly separable datasets.

## 2. Objectives

The main objectives of this project are:

* To build an end-to-end implementation of the Perceptron Learning Algorithm.
* To generate and visualize synthetic datasets (both linearly separable and non-linearly separable).
* To analyze the algorithm’s performance in terms of weight updates, convergence, and error rates.
* To experiment with hyperparameters such as learning rate, initialization of weights, and maximum iterations.

## 3. Technologies Used

* Python: Core programming language.
* NumPy: Efficient numerical operations.
* Matplotlib: Data visualization and plotting.
* Jupyter Notebook: Interactive environment for experimentation.

## 4. Dataset Description

Three datasets were generated synthetically for experimentation:

1. Linearly Separable Data – two well-separated clusters that can be divided by a straight line.
2. Non-Linearly Separable Data – same clusters with added noise to introduce overlap.
3. Test Data – a small random dataset to evaluate generalization performance.

## 5. Methodology

**Step 1: Data Generation** – Created two Gaussian-distributed clusters of points for separable data, introduced noise for overlapping data, and generated an independent test dataset.
**Step 2: Visualization** – Plotted the datasets to visually confirm separability and overlap.
**Step 3: Perceptron Implementation** – Added a bias term, initialized weights, and updated iteratively whenever a misclassified point was found:
w ← w + η·yᵢ·xᵢ
Stopping condition: either all points correctly classified or maximum iterations reached.
**Step 4: Model Evaluation** – Used a misclassification error metric to calculate training and test performance, while recording the number of updates and iterations before convergence.

## 6. Results

**Linearly Separable Data** – The perceptron converged successfully within a few iterations, achieving 0% training error. Test error was low but not zero due to differences in the generated test data.

Sample Output:

```
--- Linearly Separable Data ---
Final decision boundary: [-0.9   1.84   1.62]
Total weight updates:    1
Total iterations:        2
Training error:          0.00%
Test error:              20.00%
```

**Non-Linearly Separable Data** – The perceptron struggled to converge because of overlapping classes. Training error occasionally dropped but was unstable, and test error remained high.

Sample Output:

```
--- Non-Linearly Separable Data ---
Final decision boundary: [-9.9   8.23   7.62]
Total weight updates:    68
Total iterations:        40
Training error:          0.00%
Test error:              50.00%
```

## 7. Key Findings

* PLA works very well on linearly separable datasets, converging quickly.
* On non-separable datasets, it fails to converge and produces poor test accuracy.
* The algorithm is highly sensitive to separability and initialization.

## 8. Future Work

* Implement Kernel Perceptron to handle non-linear boundaries.
* Compare PLA with Logistic Regression and Support Vector Machines (SVM).
* Explore adaptive learning rates or mini-batch updates for stability.
* Apply the method on real-world datasets.

## 9. Conclusion

The project highlights both the strengths and weaknesses of the Perceptron Learning Algorithm. While it is effective and efficient for linearly separable datasets, its inability to handle non-linear separability underscores the importance of more advanced algorithms such as SVMs or deep learning methods in practical applications.

## 10. References

* Rosenblatt, F. (1958). The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain.
* Bishop, C. M. (2006). *Pattern Recognition and Machine Learning*. Springer.
