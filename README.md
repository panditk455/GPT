#LLM BY SCRATCH:

This project focuses on setting up a Python environment for natural language processing and deep learning using PyTorch. The initial steps involve creating and activating a Python virtual environment, followed by installing essential libraries such as `matplotlib`, `numpy`, `pylzma`, `ipykernel`, `jupyter`, and PyTorch with its related packages. Once the environment is ready, we proceed to launch Jupyter Notebook for interactive development, explore text data (specifically "Wizard of Oz"), and experiment with character-level tokenization.

We delve into various aspects of tokenization, including different types and their applications. Key concepts such as tensors, their advantages over traditional arrays, and fundamental linear algebra are introduced. The project also covers the importance of splitting data into training and validation sets, the implementation of a bigram model for text processing, and the role of batch size as a hyperparameter in model training. Additionally, we transition from CPU to GPU processing using CUDA to leverage faster computation in PyTorch.

In the latter stages, the project provides an overview of PyTorch functionalities, compares CPU versus GPU performance, and explores additional PyTorch functions. We conclude with an introduction to embedding vectors, which are crucial for representing categorical data in a continuous vector space. This structured approach ensures a comprehensive understanding of both the theoretical and practical aspects of working with text data and neural networks in PyTorch.

# CUDA Virtual Environment Setup

This guide walks you through setting up a Python virtual environment, installing necessary packages, and configuring Jupyter and VS Code for making LLM by scratch project:

## Prerequisites

Make sure you have Python installed on your system.

## Steps

### 1. Create and Activate Virtual Environment

1. **Create a Virtual Environment**:
   ```bash
   python -m venv cuda
   ```

2. **Activate the Virtual Environment**:
   - **Windows**:
     ```bash
     cuda\Scripts\activate
     ```

### 2. Install Required Packages

With the virtual environment activated, install the necessary packages:

1. **Install Basic Packages**:
   ```bash
   pip install matplotlib numpy pylzma ipykernel jupyter
   ```

2. **Install PyTorch and Related Packages**:
   Replace the URL with the appropriate one for your CUDA version if different from `cu118`.
   ```bash
   pip install torch torchvision torchaudio --index-url https://download.pytorch.org/whl/cu118
   ```

### 3. Start Jupyter Notebook

1. **Launch Jupyter Notebook**:
   ```bash
   jupyter notebook
   ```
   This will open Jupyter in your default web browser.

2. **Create a New Notebook**:
   - In the Jupyter interface, create a new notebook file named `bigram.ipynb`.

### 4. Open Project in VS Code

1. **Open VS Code** and navigate to the folder containing your Jupyter notebook. 

2. **Locate the `.ipynb_checkpoints` Directory**:
   - You will see a new directory named `.ipynb_checkpoints` which contains checkpoints of your notebook files.

### 5. Set Up Jupyter Kernel in Virtual Environment

1. **Stop the Jupyter Notebook Server** by pressing `CTRL+C` in the terminal where it's running.

2. **Install IPython Kernel**:
   ```bash
   python -m ipykernel install --user --name=cuda --display-name "cudagpt"
   ```
   This command creates a Jupyter kernel named `cudagpt` that uses the `cuda` virtual environment.

### 6. Configure PowerShell Execution Policy

1. **Set Execution Policy**:
   ```powershell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
   ```

2. **Activate the Virtual Environment in PowerShell**:
   ```powershell
   cd C:\Users\panditk\Desktop\GPT
   .\cuda\Scripts\Activate.ps1
   ```
