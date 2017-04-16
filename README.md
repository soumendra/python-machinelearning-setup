# Overview

This repository provides instructions about setting up a number of Python environments (using Anaconda) with different configurations for Scientific Computing (particularly machine learning and deep learning). Using it, you can set up the following conda environments:

| file name | environment name | description |
|-----------|------------------|-------------|
| env27.yml |   py27           | A Python environment based on 2.7.x (for machine learning) |
| env36.yml |   py36           | A Python environment based on 3.6.x (for machine learning) |
| env36tf.yml | py36tf         | A Python environment based on 3.6.x (for deep learning using tensorflow, keras) |
| env36tfgpu.yml | py36tfgpu   | A Python environment based on 3.6.x (for gpu-driven deep learning using tensorflow, keras) |

For more details on the exact packages and versions being set up, you can look at the correcponding `.yml` files.

# How to Set Up

1. Install Anaconda
2. Install necessary packages

Notes
* In the following steps, we install the environment named `py27` using the file `env27.yml`.
    - To install a different environment, change the filename appropriately in the set up instructions that follow (use `env36.yml` instead of `env27.yml`, for example).
    - If you plan to use gpus for deep learning, please note that you have to install your graphics card drivers, CUDA and cuDNN beforehand. The environments using gpu versions of packages have `gpu` at the end of their names.
* The instructions have been tested only on Ubuntu and OS X, though they should work on Windows as well (please raise a issue if you hit any snags on your Windows system).

---

## Install Anaconda

From the Anaconda [docs](http://conda.pydata.org/docs):

> Conda is an open source package management system and environment management system
for installing multiple versions of software packages and their dependencies and
switching easily between them. It works on Linux, OS X and Windows, and was created
for Python programs but can package and distribute any software.

### Overview

Using Anaconda consists of the following:

1. Install [`miniconda`](http://conda.pydata.org/miniconda.html) on your computer
2. Create a new `conda` [environment](http://conda.pydata.org/docs/using/envs.html)
3. Each time you wish to work, activate your `conda` environment


### Installation

**Download** the version of `miniconda` that matches your system. Make sure you download the version for Python 3.x (3.6 is the latest at the time of writing).

|        | Linux | Mac | Windows |
|--------|-------|-----|---------|
| 64-bit | [64-bit (bash installer)][lin64] | [64-bit (bash installer)][mac64] | [64-bit (exe installer)][win64]
| 32-bit | [32-bit (bash installer)][lin32] |  | [32-bit (exe installer)][win32]

[win64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86_64.exe
[win32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Windows-x86.exe
[mac64]: https://repo.continuum.io/miniconda/Miniconda3-latest-MacOSX-x86_64.sh
[lin64]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86_64.sh
[lin32]: https://repo.continuum.io/miniconda/Miniconda3-latest-Linux-x86.sh

**Install** [miniconda](http://conda.pydata.org/miniconda.html) on your machine. Detailed instructions:

- **Linux:** http://conda.pydata.org/docs/install/quick.html#linux-miniconda-install
- **Mac:** http://conda.pydata.org/docs/install/quick.html#os-x-miniconda-install
- **Windows:** http://conda.pydata.org/docs/install/quick.html#windows-miniconda-install


---

## Install necessary packages

**Setup** your the `py27` environment.

```sh
git clone https://github.com/soumendra/python-machinelearning-setup.git
cd python-machinelearning-setup
```

If you are on Windows, **rename**   
`meta_windows_patch.yml` to   
`meta.yml`

**Create** `py27`.  Running this command will create a new `conda` environment that is provisioned with all libraries listed above.
```
conda env create -f env27.yml
```

In case you want to install another environment, use the appropriate *yml* file. For example, to install an environment including Python 3.6.x and tensorflow (cpu version), you can run,
```
conda env create -f env36tf.yml
```


**Verify** that the `py27` environment was created in your environments:

```sh
conda info --envs
```

**Cleanup** downloaded libraries (remove tarballs, zip files, etc):

```sh
conda clean -tp
```

### Uninstalling

To uninstall the environment:

```sh
conda env remove -n py27
```

---


## Using the Anaconda environment

Now that you have created an environment, in order to use it, you will need to activate the environment. This must be done **each** time you begin a new working session, i.e., open a new terminal window.

**Activate** the `py27` environment:

### OS X and Linux
```sh
$ source activate py27
```

### Windows
Depending on shell either:
```sh
$ source activate py27
```

or

```sh
$ activate py27
```

That's it. Now all of the `py27` libraries are available to you. You can start a Jupyter Notebook with:

```sh
jupyter notebook
```

To exit the environment when you have completed your work session, simply close the terminal window.
