# Setting up AWS instance (Ubuntu)

When you are logging into a new ec2 instance for the first time:

## Basic Setup
```bash
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install -y python-dev software-properties-common curl default-jre 
sudo apt-get install -y default-jdk python-software-properties byobu vim
```
## Setup Ubuntu for Computer Vision (OpenCV)

```bash
sudo apt-get install build-essential cmake pkg-config
sudo apt-get install libjpeg8-dev libtiff5-dev libjasper-dev libpng12-dev
sudo apt-get install libgtk2.0-dev
sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev libv4l-dev
sudo apt-get install libatlas-base-dev gfortran
sudo apt-get install libboost-all-dev
sudo apt-get install python-dev

sudo apt-get install ubuntu-restricted-extras
sudo apt-get install ubuntu-restricted-addons
sudo apt-get install vlc
sudo apt-get install mencoder mplayer
```

## Setup GitHub
```bash
sudo apt-get install git git-core
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

## Setup Anaconda and an environment
* Set up anaconda - https://github.com/soumendra/python-machinelearning-setup
* clone and install from your environment of choice (mlredux.yml, greyatom.yml)

## Setup Jupyter Notebook (remote server)
```bash
jupyter notebook --generate-config
mkdir certs
cd certs
sudo openssl req -x509 -nodes -days 365 -newkey rsa:1024 -keyout mycert.pem -out mycert.pem

cd ~/.jupyter
vim jupyter_notebook_config.py
```

**Content for jupyter_notebook_config.py**:

> c = get_config()

> c.NotebookApp.certfile = u'/home/ubuntu/certs/mycert.pem'

> c.NotebookApp.ip = '*'

> c.NotebookApp.open_browser = False 

> c.NotebookApp.port = 8888
