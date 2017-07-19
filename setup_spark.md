# Set up Spark

## Install Java

Check if `Java` sdk is installed in your system. If not, follow the following instructions (for Ubuntu only, mac folks can do `brew install java` and windows folks can just download and execute the binary)

```bash
sudo apt-get update
sudo apt-get -y upgrade
```

```bash
sudo apt-get install -y software-properties-common curl
sudo apt-get install default-jre default-jdk
```

## Java Alternative (optional)

 
* **Please note that Java was installed in the last section, and don't actually need to go through this section to install Java.**
* **This is for adventurous students who wish to install the jdk/jre from Oracle (if you don't know what I am talking about, you don't need to do it.**

```bash
sudo apt-get install python-software-properties
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update

sudo apt-get install oracle-java8-installer
```

If the Oracle version is the only one you have installed, then you have only one Java framework installed i your system. Otherwise, if you have multiple Java frameworks installed in your system, you can choose one of them with the following:

```bash
sudo update-alternatives --config java
sudo update-alternatives --config javac
```

And here is how you can set up your JAVA_HOME

* Note in the install path from (the command above)
        sudo update-alternatives --config java
* Add JAVA_HOME="YOUR_PATH" to /etc/environment
        source /etc/environment
        echo $JAVA_HOME
        
# Configuring Spark, findspark and pySpark

In case you work with Anaconda environments,

```bash
source activate <your-favourite-environment's-name>
```

After executing that in the terminal, follow the instructions in 
[these slides](http://nbviewer.jupyter.org/github/soumendra/spark_machine_learning_tutorial/blob/master/Slides/Spark02-%20Setting%20Up%20Spark%2C%20PySpark%20and%20Notebook.pdf).

---
