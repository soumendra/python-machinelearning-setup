# Setting up AWS instance

When you are logging into a new ec2 instance for the first time:

**Basic Setup**
```bash
sudo apt-get update -y
sudo apt-get upgrade -y
sudo apt-get install -y python-dev software-properties-common curl default-jre 
sudo apt-get install -y default-jdk python-software-properties byobu vim
```

**Setup GitHub**
```bash
sudo apt-get install git git-core
git config --global user.email "you@example.com"
git config --global user.name "Your Name"
```

**Setup Anaconda and an environment**
* Set up anaconda - https://github.com/soumendra/python-machinelearning-setup
* clone and install from your environment of choice (mlredux.yml, greyatom.yml)

**Setup Jupyter Notebook (remote server)
```bash
jupyter notebook --generate-config
mkdir certs
cd certs
cd ~/.jupyter
vim jupyter_notebook_config.py
```

**Content for jupyter_notebook_config.py**:

> c = get_config()

> c.NotebookApp.certfile = u'/home/ubuntu/certs/mycert.pem'

> c.NotebookApp.ip = '*'

> c.NotebookApp.open_browser = False 

> c.NotebookApp.port = 8888
