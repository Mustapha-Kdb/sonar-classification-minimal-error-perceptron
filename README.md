# 📡 Robust Sonar Classification: Minim-Error Perceptron

This repository implements a **Minim-Error Perceptron** approach to solve the binary classification problem of the Sonar Dataset (discriminating between metal cylinders and rocks).

Unlike the standard Perceptron, which may stop as soon as it finds any separating hyperplane, this implementation focuses on **minimizing the misclassification count** and analyzing the **geometric stability** of the decision boundary to ensure better generalization.

## 🎯 Project Objectives

* **Error Minimization:** Fine-tuning the perceptron learning rule to achieve the lowest possible training ($E_a$) and generalization ($E_g$) errors.
* **Stability Analysis:** Calculating the geometric margin ($\gamma$) for each test sample to evaluate the confidence level of the classifications.
* **Performance Benchmarking:** Visualizing error convergence over epochs to ensure the model reaches a stable state.

## ⚙️ Key Technical Features

* **Advanced Data Processing:** Custom regex-based parsing of raw `.mines` and `.rocks` sonar data.
* **Minim-Error Logic:** An optimized training loop designed to keep the weight vector that yields the minimum error during the learning process.
* **Stability Visualization:** * **Convergence Plot:** Tracking the decrease of misclassifications over time.
    * **Stability Bar Chart:** A detailed view of the distance of each test example from the decision boundary, identifying "well-classified" vs "misclassified" samples.

## 📊 Performance & Results

The model achieves high accuracy by focusing on the examples closest to the boundary.
* **Learning Error ($E_a$):** Optimized through iterative updates.
* **Generalization Error ($E_g$):** Evaluated on unseen test data to confirm the robustness of the minimal error approach.

## 🛠️ Tech Stack
* **Language:** Python 3
* **Libraries:** `NumPy` for vector operations, `Matplotlib` for stability and convergence visualization, `Pandas` for data management.

## 🚀 How to use
1. Ensure your data files (`sonar.rocks` and `sonar.mines`) are in the `data/` directory.
2. Run the `MinimErrorPerceptron-1T.ipynb` notebook.
3. Observe the stability charts to see how well the model handles difficult-to-classify signals.
