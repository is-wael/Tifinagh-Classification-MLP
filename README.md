# Multi-class Classification of Handwritten Tifinagh Characters

![Python 3.8+](https://img.shields.io/badge/python-3.8+-blue.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## Project Overview

This project presents a comprehensive implementation of a Multilayer Perceptron (MLP) neural network built from scratch using only Python and NumPy. The model is designed for the multi-class classification of the 33 characters of the Amazigh (Berber) Tifinagh alphabet, trained and evaluated on the **Amazigh Handwritten Character Database (AMHCD)**.

The primary goal is to demonstrate a deep, fundamental understanding of neural network mechanics, from the mathematical foundations to practical implementation and robust evaluation. The project incorporates modern deep learning techniques to ensure high performance and stability.

A detailed academic report in LaTeX format can be found in the `/report` directory.

## Key Features

- **"From Scratch" Implementation**: The entire neural network (forward/backward propagation, loss function) is built using only NumPy. No high-level frameworks like TensorFlow or PyTorch were used for the core model.
- **Multilayer Perceptron Architecture**: A 1024-64-32-33 architecture with ReLU activations in the hidden layers and a Softmax output layer.
- **Adam Optimizer**: Implementation of the Adam optimization algorithm for efficient and adaptive learning rate convergence.
- **L2 Regularization**: A regularization term is included in the cost function to prevent overfitting.
- **Data Augmentation**: The training set is augmented with on-the-fly random rotations and translations to improve model generalization.
- **Robust Evaluation**: The model's performance is rigorously assessed using a 5-fold Stratified Cross-Validation to ensure stability and reliability of the results.

## Installation and Setup

To run this project, it is recommended to use a virtual environment.

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/is-wael/Tifinagh-Classification-MLP.git](https://github.com/is-wael/Tifinagh-Classification-MLP.git)
    cd Tifinagh-Classification-MLP
    ```

2.  **Create and activate a virtual environment (optional but recommended):**
    ```bash
    python3 -m venv env
    source env/bin/activate
    ```

3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *Note: If you are not using Google Colab, you may need to install Graphviz at the system level for the architecture visualization to work.*
    ```bash
    # On Debian/Ubuntu
    sudo apt-get install graphviz
    ```

## How to Run the Code

The project is contained within a single Jupyter Notebook (`main.ipynb`) located in the `/notebooks` directory.

1.  **Kaggle API Credentials**: The notebook automatically downloads the required dataset from Kaggle. For this to work, you need to have a `kaggle.json` API token. When you run the first code cell, it will prompt you to upload this file.
    - You can generate your `kaggle.json` file from your Kaggle account page under `Account` -> `API` -> `Create New API Token`.

2.  **Execute the Notebook**: Open and run the cells in `notebooks/main.ipynb` using Jupyter Notebook, JupyterLab, or by uploading it to Google Colab.

The notebook will handle data download, preprocessing, model training, evaluation, and the generation of all figures and results.

## Project Structure

```
.
├── .gitignore
├── README.md
├── requirements.txt
├── notebooks/
│   └── main.ipynb
└── report/
    ├── rapport.tex
    └── figures/
        └── ... (PNG images for the report)
```

-   **`/notebooks/`**: Contains the main Jupyter Notebook with all the Python code.
-   **`/report/`**: Contains the LaTeX source file (`.tex`) and a subdirectory for figures (`.png`).
-   **`README.md`**: This file.
-   **`.gitignore`**: Specifies which files for Git to ignore.
-   **`requirements.txt`**: Lists the required Python packages.

## Results Summary

The model achieves a high and stable performance, validated through a rigorous 5-fold stratified cross-validation process.

-   **Mean Accuracy**: **~90.7%**
-   **Standard Deviation**: **~0.64%**

The low standard deviation confirms the model's robustness. The detailed learning curves and confusion matrix analysis can be found in the full report.
