Below are setup instructions for the Big Data course. You will need to
complete the setup steps below to install the necessary software on your
machine. First, make sure to clone this repository so you have all the files. If you are not familiar with git you should install it here: https://git-scm.com/

`git clone http://gitlab.cambridgespark.com/pub/bigdata.git`


## Setup

There are a few things to install: Anaconda (a Python distribution), Apache
Spark (a distributed computation framework) and a dataset.


### Install Python

Install Anaconda (**Python 2.7**) from:  [https://www.continuum.io/downloads](https://www.continuum.io/downloads).
This includes python 2.7.9 and the necessary libraries we will be using: `numpy` and `matplotplib`.


### Install Java

Install **Java 8** if you don't have it already from [http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

You need the ```Java SE Development Kit```.

### Create a directory for your project

Create a fresh directory on the place of your choice on your computer. In this
directory you will place some software as well as data. You will also store
your own programs in there.

If you have already created one to hold these instructions, feel free to use
it.


### Download Apache Spark

Download Apache Spark 2.1.0 from: [http://spark.apache.org/downloads.html](http://spark.apache.org/downloads.html). Place `spark-2.1.0-bin-hadoop2.7.tgz` in your project directory and extract it.

On Windows, you can extract `tgz` files using 7-zip – available from [http://www.7-zip.org/](http://www.7-zip.org/).

### Download the dataset

Download the file
[https://s3-eu-west-1.amazonaws.com/com.cambridgespark.content/courses/big-data/sets/HNStories.json.bz2](https://s3-eu-west-1.amazonaws.com/com.cambridgespark.content/courses/big-data/sets/HNStories.json.bz2). Place `HNStories.json.bz2` in your project directory and extract it.

7-zip (mentioned above) is also able to extract `bz2` files.

## Test

### OSX and Linux

Open a terminal in your project directory and run the following command:

```
export PYSPARK_DRIVER_PYTHON=ipython
export PYSPARK_DRIVER_PYTHON_OPTS=notebook
./spark-2.1.0-bin-hadoop2.7/bin/pyspark
```

This should open an ipython notebook. Use it to open the file `load_libraries.ipynb`. Execute the first cell to make sure you have all of the require libraries.

### Windows

You will need to set environment variables so PySpark can run as a iPython notebook.

Here's a tutorial explaining how ot set environment variables on Windows if you have never done this before: http://www.computerhope.com/issues/ch000549.htm

Once you've familiarised yourself with this tutorial you need to set the following environment variables:

`PYSPARK_DRIVER_PYTHON` with the value of `ipython`

`PYSPARK_DRIVER_PYTHON_OPTS` with the value of `notebook`

Open a shell (`cmd`) in your project's directory and execute:
```
spark-2.1.0 -bin-hadoop2.7\bin\pyspark
```

This should open an ipython notebook. Use it to open the file `load_libraries.ipynb`. Execute the first cell to make sure you have all of the require libraries.
