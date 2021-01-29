# How to install Anaconda on Ubuntu 20.04

## Introduction
Designed for data science and machine learning workflows, Anaconda is an open-source package manager, environment manager, and distribution of the Python and R programming languages.

## Step 1: Retrieve the Latest Version of Anaconda
From a web browser, go to the Anaconda Distribution page, available via the following [link](https://www.anaconda.com/distribution/).

## Step 2: Download the Anaconda Bash Script
First, move into the /tmp directory and use curl to download the link you copied from the Anaconda website:

``` bash

cd /tmp
sudo apt install curl -y
curl -O https://repo.anaconda.com/archive/Anaconda3-2020.11-Linux-x86_64.sh

```

## Step 3: Verify the Data Integrity of the Installer

Ensure the integrity of the installer with cryptographic hash verification through SHA-256 checksum:

``` bash

sha256sum Anaconda3-2020.11-Linux-x86_64.sh

```

## Step 4: Run the Anaconda Script

``` bash

bash Anaconda3-2020.11-Linux-x86_64.sh

```

You’ll receive the following output to review the license agreement by pressing ENTER until you reach the end.

When you get to the end of the license, type yes as long as you agree to the license to complete installation.

## Step 5: Complete Installation Process

Once you agree to the license, you will be prompted to choose the location of the installation. You can press ENTER to accept the default location or specify a different location.


At this point, the installation will proceed. Note that the installation process takes some time.

## Step 6 — Select Options

Once installation is complete, you’ll receive the following output:


It is recommended that you type yes to use the conda command.

## Step 7 — Activate Installation

You can now activate the installation with the following command:	

``` bash

source ~/.bashrc

```

## Step 8 — Test Installation

Use the conda command to test the installation and activation:

``` bash

conda list

```

You’ll receive output of all the packages you have available through the Anaconda installation.

## Step 9 — Set Up Anaconda Environments

You can create Anaconda environments with the conda create command. For example, a Python 3 environment named my_env can be created with the following command:

``` bash

conda create –name my_env python=3

```

Activate the new environment like so:

``` bash

conda activate my_env

```

Your command prompt prefix will change to reflect that you are in an active Anaconda environment, and you are now ready to begin work on a project.

## Step 10: Installing the necessary python packages

Most Python packages are now designed to be compatible with Python’s pip package manager.

### Tensorflow – Cpu

TensorFlow is an end-to-end open-source platform for machine learning. It has a comprehensive, flexible ecosystem of tools, libraries and community resources that lets researchers push the state-of-the-art in ML and developers easily build and deploy ML powered applications.

``` bash

pip install tensorflow

```

### Cvxopt (Convex Optimisation)

CVXOPT is a free software package for convex optimization based on the Python programming language. It can be used with the interactive Python interpreter, on the command line by executing Python scripts, or integrated in other software via Python extension modules. Its main purpose is to make the development of software for convex optimization applications straightforward by building on Python’s extensive standard library and on the strengths of Python as a high-level programming language.

``` bash

pip install cvxopt

```

### Sckit-learn

Scikit-learn provides a range of supervised and unsupervised learning algorithms via a consistent interface in Python.
It is licensed under a permissive simplified BSD license and is distributed under many Linux distributions, encouraging academic and commercial use.

The library is built upon the SciPy (Scientific Python) that must be installed before you can use scikit-learn. This stack that includes:
- NumPy: Base n-dimensional array package
-	SciPy: Fundamental library for scientific computing
-	Matplotlib: Comprehensive 2D/3D plotting
-	IPython: Enhanced interactive console
-	Sympy: Symbolic mathematics
-	Pandas: Data structures and analysis

Extensions or modules for SciPy care conventionally named SciKits. As such, the module provides learning algorithms and is named scikit-learn.

The vision for the library is a level of robustness and support required for use in production systems. This means a deep focus on concerns such as ease of use, code quality, collaboration, documentation and performance.


``` bash

pip install scikit-learn

```

### OpenCV

OpenCV is a cross-platform library using which we can develop real-time computer vision applications. It mainly focuses on image processing, video capture and analysis including features like face detection and object detection.


``` bash

pip install opencv-python

```
