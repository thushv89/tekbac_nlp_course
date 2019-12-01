## Operating System, Software and Hardware Requirements
* Operating system: Windows 10
* RAM: Recommended 8GB
* Disk space: 5GB-10GB
* Python: 3.5
* (GPU) Cuda Toolkit: 10.0 (Make sure you have all the [Software Requirements](https://www.tensorflow.org/install/gpu) for TensorFlow)

## Creating the `conda` Environment for the TEKBAC Workshop

1. Download and install [Anaconda](https://repo.continuum.io/archive/Anaconda3-4.2.0-Windows-x86_64.exe) or [Anaconda (32-bit)](https://repo.continuum.io/archive/Anaconda3-4.2.0-Windows-x86.exe)
2. Make sure conda is in the system `PATH` by trying `conda --version` in the command prompt
3. Create a conda virtual environment using `conda create -n tekbac.nlp python=3.5`
4. cd into the `<project directory>`
5. Activate the newly created environment with `activate tekbac.nlp`
6. Install the required libraries by typing the following in the command prompt
7. If you **do not have a GPU** use: `pip install -r requirements.txt`
8. If you **do have a GPU** use: `pip install -r requirements_gpu.txt`

## Activating the `conda` Environment`
1. Activate the newly created environment with `activate tekbac.nlp`
2. If successfully activated, your prompt in the command line should show `(tekbac.nlp) C:\Users\X\Documents`, instead of showing the directory you are in (e.g. `C:\Users\X\Documents`)

## Validating Jupyter notebook works
1. Go to your code directory and activate the `conda` environment in the terminal.
2. Next, type in `jupyter notebook`
3. Open the `test_setup.ipynb`
4. You should be able to run all the cells in the notebook without any errors. 

**Note**: If you're having trouble running this, post an issue [here](https://github.com/thushv89/tekbac_nlp_course/issues). Your issue needs to contain, all the software versions of things listed above, what you tried so far (step by step), the error message you're getting, a screenshot of the error.

## Validating the installed packages
1. After activating the `conda` environment, type in `python`
2. Try to import the packages 
  * `numpy` with `import numpy as np`, 
  * `pandas` with `import pandas as pd`, 
  * `tensorflow` with `import tensorflow as tf`, 
  * `matplotlib` with `import matplotlib`, 
  * `scikit-learn` with `import sklearn`, 
  * `Pillow` with `import PIL`
  * `nltk` with `import nltk`
3. Finally make sure you do not get any errors when importing the above packages as well as you can see the version of each package by typing `print(<package>.__version__)`

## Checking if GPU is identified by TensorFlow (If the laptop has one)
1. After activating the `conda` environment, type in `python`
2. Import TensorFlow with `import tensorflow as tf`
2. Type in `print(tf.test.is_gpu_available())` and see if it prints out `True`

## Deactivating the `conda` Environment
1. Deactivate the conda environment with `deactivate`
2. If successfully deactivated your prompt in the command line should appear normally again (e.g. `C:\Users\X\Documents`)

## Installing packages not listed in the `requirements.txt`

If you need to install a custom package, enter the following command in the command prompt `conda install -n tekbac.nlp <package>`



Further reading on how to setup conda environments: [Here](https://uoa-eresearch.github.io/eresearch-cookbook/recipe/2014/11/20/conda/)