# Hadoop-versus-Python
Comparative Analysis Study of Hadoop (Distributed) and Python (Serial) Execution for Big Data Set. 
A dataset text file of Sales is taken which contains six columns separated by a tab which include date, time, store, item, cost, payment. 
The aim is to find the time taken by Hadoop and Python for executing the same task. 
Task - Finding Total Cost for every Store.

Dataset Link: https://drive.google.com/file/d/17ieMcpnkGp06Nbd2Jx8W8T3cH11E2dYI/view?usp=sharing

Upload data to hadoop HDFS

Command

<b>hadoop fs -mkdir myinput 

hadoop fs -put purchases.txt myinput</b>

Navigate to the code folder with the mapper.py and reducer.py

<b>hs mapper.py reducer.py myinput output1 </b> *//hs used for hadoop streaming as Python used instead of default Java*

Output saved in the dir output1

Command to view
<b>hadoop fs -cat output1/part-00000 | less</b> 

# PYTHON

run python using python mapper.py, sort.py and reducer.py in order from the Python folder. (Python 2.6)
