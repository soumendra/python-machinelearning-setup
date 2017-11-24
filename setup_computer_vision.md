# Ubuntu

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
```

# macos

Install the following:

* xcode
* xcode clt
* homebrew

```bash
brew install boost
brew install boost-python
brew list | grep 'boost'
    > boost
    > boost-python
brew tap homebrew/science
brew install opencv3
```

# Installing the conda environment

After cloning this repo:

```bash
conda env create -f cv.yml
```
