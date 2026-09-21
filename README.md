# Task 6: Introduction to Deep Learning & Artificial Neural Networks (ANN)

This repository contains the code, diagnostic visualizations, and technical report for Task 6 of the Artificial Intelligence & Machine Learning Lab. The project transitions from traditional machine learning to deep learning by implementing a multi-layer Artificial Neural Network (ANN) using TensorFlow and Keras to classify clinical breast mass data.

## Project Objective
The primary goal is to build, compile, and train a Deep Learning model to perform binary classification on the Breast Cancer Wisconsin (Diagnostic) dataset. The pipeline evaluates the model's accuracy and loss convergence and establishes a benchmark comparison against baseline models from previous tasks (Logistic Regression and Random Forest).

## Tech Stack & Tools
* **Language:** Python 3
* **Frameworks:** TensorFlow 2.x, Keras, Scikit-Learn
* **Data Processing & Math:** Pandas, NumPy
* **Visualization:** Matplotlib, Seaborn
* **Environment:** Google Colab

## Key Engineering Highlights
* **Feature Scaling:** Applied `StandardScaler` to normalize the 30 continuous clinical features, ensuring stable gradient descent optimization.
* **Network Architecture:** Designed a Multi-Layer Perceptron (MLP) using the `Sequential` API with `Dense` layers, utilizing `ReLU` activations for hidden layers and `Sigmoid` for the final binary probabilistic mapping.
* **Regularization:** Integrated `Dropout` layers (20% rate) to prevent the network from complex co-adaptations and overfitting on the small training set.
* **Optimization:** Utilized the `Adam` optimizer and `binary_crossentropy` loss function.
* **Resource Efficiency:** Configured an `EarlyStopping` callback to monitor validation loss and automatically halt training when convergence is reached, restoring the best model weights.

## Repository Structure
* `Task_6_Deep_Learning.ipynb`: The main Google Colab Jupyter Notebook containing the data pipeline, network architecture, training loop, and automated ML vs. DL comparisons.
* `Task_6_Report_Suyash_Dixit.pdf`: The comprehensive technical project report detailing the theoretical mathematical framework, diagnostic error interpretation, and strategic conclusions.

## Performance Benchmark
| Model Type | Algorithm | Optimization / Configuration | Test Accuracy |
| :--- | :--- | :--- | :--- |
| **Deep Learning** (Task 6) | Artificial Neural Network | Adam, Dropout (0.2), Early Stopping | **~97.3%** |
| **Linear ML** (Task 4) | Logistic Regression | L2 Penalty, L-BFGS Solver | **~97.3%** |
| **Ensemble ML** (Task 5) | Random Forest | 100 Estimators, Bootstrap Aggregation | **~96.4%** |

*The results indicate that while the ANN successfully converges to identify non-linear decision boundaries, optimized traditional linear models provide an exceptionally strong baseline for this specific structured, low-dimensional tabular dataset.*
