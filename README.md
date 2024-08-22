
# LLM BY SCRATCH 

This project is all about setting up a Python environment for natural language processing and deep learning using PyTorch. We start by creating and activating a Python virtual environment and installing key libraries like `matplotlib`, `numpy`, `pylzma`, `ipykernel`, `jupyter`, and PyTorch. Once that's done, we launch Jupyter Notebook to work interactively with text data from "Wizard of Oz" and try out character-level tokenization. We cover various aspects of tokenization, introduce tensors and their benefits, and explain fundamental linear algebra concepts. We also discuss how to split data into training and validation sets, implement a bigram model, and manage batch sizes during training. Later, we explore GPU processing with CUDA for faster computations, compare CPU and GPU performance, and dive into PyTorch’s functionalities and embedding vectors for representing data in a continuous space. This structured approach helps in understanding both the theory and practical aspects of working with text data and neural networks using PyTorch.


# CUDA Virtual Environment Setup

This guide will walk you through setting up a Python virtual environment, installing necessary packages, and configuring Jupyter and VS Code for a project focused on creating an LLM from scratch.

## Prerequisites

Ensure you have Python installed on your system.

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
   - **macOS/Linux**:
     ```bash
     source cuda/bin/activate
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
   This command will open Jupyter in your default web browser.

2. **Create a New Notebook**:
   - In the Jupyter interface, create a new notebook file named `bigram.ipynb`.

### 4. Open Project in VS Code

1. **Open VS Code** and navigate to the folder containing your Jupyter notebook.

2. **Locate the `.ipynb_checkpoints` Directory**:
   - You will see a directory named `.ipynb_checkpoints` which contains checkpoints of your notebook files.

### 5. Set Up Jupyter Kernel in Virtual Environment

1. **Stop the Jupyter Notebook Server** by pressing `CTRL+C` in the terminal where it's running.

2. **Install IPython Kernel**:
   ```bash
   python -m ipykernel install --user --name=cuda --display-name "cudagpt"
   ```
   This command creates a Jupyter kernel named `cudagpt` that uses the `cuda` virtual environment.

### 6. Configure PowerShell Execution Policy (Windows Users)

1. **Set Execution Policy**:
   ```powershell
   Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope Process
   ```

2. **Activate the Virtual Environment in PowerShell**:
   ```powershell
   cd path\to\your\project
   .\cuda\Scripts\Activate.ps1
   ```

Replace `path\to\your\project` with the path to the directory where your project is located.

