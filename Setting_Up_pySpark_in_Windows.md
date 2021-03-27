# Setting up pySpark in Windows

## Step 1 - Download and Install

<ul>
    <li>Download <a href ='https://www.python.org/downloads/release/python-375/'>python 3.7.5</a></li>
    <li>Download <a href ='https://jdk.java.net/java-se-ri/8-MR3'>openjdk-8-jdk-headless/openjdk-8u41-b04-windows-i586-14_jan_2020</a></li>
    <li>Download <a href ='https://spark.apache.org/downloads.html'>spark-2.4.7-bin-hadoop2.7</a></li>
</ul>

`Note`: Dont forget to add python to Path while installing, there will be a checkbox in the start of installation.

## Step 2 - Set up Environment Variables

Add 
<ul>
    <li>JAVA_HOME: __urPath__\java-se-8u41-ri</li>
    <li>SPARK_HOME: __urPath__\spark-2.4.7-bin-hadoop2.7</li>
    <li>HADOOP_HOME: __urPath__\spark-2.4.7-bin-hadoop2.7</li>
</ul>

Also Add
<ul>
    <li>Path: __urPath__\spark-2.4.7-bin-hadoop2.7\bin</li>
    <li>Path: __urPath__\java-se-8u41-ri\bin</li>
</ul>
    
You can add this in 'User Variables'

## Step 3 - Test installation

Open cmd and Run
<ul>
    <li>python --version</li>
    <li>java -version</li>
    <li>pyspark --version</li>
</ul>

## Step 4 - Download a HDFS dependency

<ul>
    <li><a href='https://github.com/4ttty/winutils/blob/master/hadoop-2.7.1/bin/winutils.exe'>Download winutils</a></li>
    <li>Paste the 'winutlis.exe' in '__urPath__\spark-2.4.7-bin-hadoop2.7\bin' location</li>
</ul>

## Step 5 - Launch

Setup a virtual python env and launch jupyter-lab

```
import findspark
findspark.init()

import pyspark
```
`Note`: Remember to "pip install -r requirements.txt"


There you go, your spark installation in Windows