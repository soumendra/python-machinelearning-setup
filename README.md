# Overview

This repository contains setup instructions for various python machine learning environments I use. Since a lot of people/computers have to replicate my environments quite often, I have tried to put detailed instructions in one place (here). It mainly cover

* [How to setup your python programming environment in a replicable manner](https://github.com/soumendra/python-machinelearning-setup/blob/master/setup_environments.md)
* [How to set up your aws instance from scratch](https://github.com/soumendra/python-machinelearning-setup/blob/master/setup_aws.md)
    - AMIs are great, but sometimes there is no good fit
    - Most often, even when I'm using an AMI with preloaded software, I still have to configure a few things (and I like setting up my own conda enviroment - see the guide above)
    - You can also follow this to set up your brand new Ubuntu installation
* [How to setup your Ubuntu/MacOS system for Computer Vision (mainly OpenCV3](https://github.com/soumendra/python-machinelearning-setup/blob/master/setup_computer_vision.md)
* [How to set up Spark in Ubuntu and MacOS]()

# Available Python environments (Anaconda)

* [How to setup your python programming environment in a replicable manner](https://github.com/soumendra/python-machinelearning-setup/blob/master/setup_environments.md)

Here is a list of environments available through the guide above:

| file name | environment name | description |
|-----------|------------------|-------------|
|  py27.yml |   py27           | A Python environment based on 2.7.x (for machine learning) |
|  py35.yml |   py35           | A Python environment based on 3.5.2 (for machine learning) |
|  py36.yml |   py36           | A Python environment based on 3.6.x (for machine learning) |
|  py36tf.yml | py36tf         | A Python environment based on 3.6.x (for deep learning using tensorflow, keras) |
|  py36tfgpu.yml | py36tfgpu   | A Python environment based on 3.6.x (for gpu-driven deep learning using tensorflow, keras) |
| mlredux.yml | mlredux        | A Python environment based on 3.5.2 (for machine learning) |
| scratchpad.yml | scratchpad  | A Python 3.5.2 environment that has a lot of libraries for doing a lot of things |
| cv.yml         | cv          | A Python 3.5.2 environment for computer vision |
| greyatom.yml   | greyatom    | A Python 2.7.x environment for the greyatom curriculum |
| bdap.yml       | bdap        | A Python 3.5.2 environment for bdap curriculum (except for deep learning and computer vision, for Spark, Machine Learning (sklearn) etc) |

For more details on the exact packages and versions being set up, you can look at the correcponding `.yml` files.
