# Optimization Algorithms Comparison
## 📖 Project Overview

In this project, we compare and analyze the performance of five different optimization algorithms applied to two distinct models:

1. **Univariate Linear Regression** with varying polynomial degrees and training set sizes.
2. **Intent Classification (Neural Network)** using the ATIS dataset for a classification task.

The optimization algorithms evaluated in this study include:
- **Gradient Descent (GD)**
- **Stochastic Gradient Descent (SGD)**
- **Gradient Descent with Momentum**
- **RMSProp**
- **Adam Optimizer**

## 🔍 Objectives

The key objectives of this project were:
- To explore how different optimization algorithms perform under various conditions, such as polynomial degrees and training set sizes in linear regression.
- To evaluate how the optimizers behave when applied to a neural network for a classification task on the ATIS dataset.
- To compare convergence speed, stability, and the final loss to determine the best optimizer for both linear regression and neural network tasks.

## 🧑‍💻 Key Features

### 1. **Model 1: Univariate Linear Regression**
- **Polynomial Degrees:** 1, 2, 3, 4
- **Training Set Sizes:** Varied
- **Objective:** To evaluate the performance of optimization algorithms under different complexities and dataset sizes.
- **Key Findings:**  
    - **Gradient Descent (GD):** Slow convergence, often getting stuck in local minima, especially with higher polynomial degrees.
    - **Stochastic Gradient Descent (SGD):** Faster convergence but introduces oscillations, particularly with larger learning rates.
    - **Momentum:** Enhanced convergence by reducing oscillations, outperforming GD and SGD.
    - **RMSProp:** Superior convergence, adaptive to learning rates, outperforms other algorithms in terms of speed.
    - **Adam Optimizer:** Best overall performance, combining the strengths of both Momentum and RMSProp.

### 2. **Model 2: Intent Classification with Neural Networks**
- **Dataset:** ATIS (Airline Travel Information System)
- **Objective:** To evaluate how optimization algorithms handle neural network training on a classification task.
- **Key Findings:**  
    - **SGD:** Slow convergence with higher final loss, demonstrating instability during training.
    - **SGD with Momentum:** Faster convergence than SGD, but still lacked the stability of more advanced methods.
    - **RMSProp:** Smooth convergence with lower loss, demonstrating its adaptive learning rate as a key advantage.
    - **Adam:** Fastest convergence and lowest final loss, showing clear superiority in terms of performance and efficiency.

## 🚀 Optimizers Performance

The following summarizes the performance of each optimizer:

| Optimizer                   | Key Characteristics                                           | Performance Summary                 |
|-----------------------------|---------------------------------------------------------------|-------------------------------------|
| **Gradient Descent (GD)**    | Simple, consistent updates.                                   | Slow convergence; prone to local minima. |
| **Stochastic Gradient Descent (SGD)** | Faster updates with noisy gradients.                         | Fast convergence, but prone to instability and oscillations. |
| **Momentum**                 | Smoothing updates by adding momentum to previous gradients.   | Improved convergence over GD and SGD, reducing oscillations. |
| **RMSProp**                  | Adaptive learning rate per parameter.                         | Fast convergence with adaptive learning rate, avoiding overshooting. |
| **Adam Optimizer**           | Combines Momentum and RMSProp techniques.                     | Best performance overall, fast convergence, and stable final loss. |

## 🧠 Analysis and Findings

- **Gradient Descent vs. SGD:**  
    - **GD** performs well on small datasets but struggles with more complex models due to its slow convergence, especially in high-dimensional spaces.
    - **SGD**, while faster, can exhibit instability, particularly when the learning rate is too high. However, it performs better on large datasets where individual updates are more beneficial.

- **Momentum and Its Benefits:**  
    - **Momentum** helps smooth out the oscillations of SGD and can drastically improve convergence speed, especially when dealing with complex or noisy datasets.

- **RMSProp and Adaptive Learning Rates:**  
    - **RMSProp** adjusts the learning rate dynamically, providing a significant advantage over SGD and basic Momentum in terms of stability and speed. This makes it particularly suited for complex models and large datasets.

- **Adam Optimizer's Superiority:**  
    - **Adam** optimizer combines the benefits of **Momentum** and **RMSProp**, delivering superior results in terms of both convergence speed and final accuracy. It is the preferred choice for both regression and neural network tasks due to its robustness and efficiency.

## 🔧 How to Use

To run the comparison and see the optimizer performances yourself, follow these steps:

1. **Clone the repository:**
    ```bash
    git clone https://github.com/your-username/optimization-algorithms-comparison.git
    ```

2. **Install dependencies:**
    - Make sure to have Python installed.
    - Install required libraries:
    ```bash
    pip install -r requirements.txt
    ```

3. **Run the models:**
    - Navigate to the directory and run the models:
    ```bash
    python linear_regression.py
    python neural_network.py
    ```

## 📊 Results

The detailed results, including training loss graphs, comparison plots, and algorithm-specific performance data, can be found in the **`results`** folder.

## 📝 Conclusion

The results from this project demonstrate that advanced optimizers like **Adam** significantly outperform traditional methods like **Gradient Descent** and **Stochastic Gradient Descent**. **Momentum** and **RMSProp** also show considerable improvements over basic SGD, especially in terms of stability and convergence speed. **Adam**'s combination of the benefits from both Momentum and RMSProp makes it the top choice for both **univariate linear regression** and **neural network classification** tasks.

### 🛠️ Future Work:
- Expand dataset size for further testing.
- Explore additional neural network architectures and optimizers.
- Experiment with hyperparameter tuning for even better results.

## 👨‍💻 Contribution

Feel free to fork this project, raise issues, or make contributions by submitting pull requests. Contributions are welcome to enhance the model performance and explore other optimization techniques.

---

**License**: This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
