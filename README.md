# hadoop-hands-on

To compile the word count:
bin/hadoop com.sun.tools.javac.Main WordCount.java

Build Jar:
jar cf wc.jar WordCount*.class

Data File: words.txt
java,python,scala,spark
aws,azure,oracle
java,aws,scala
python,scala

Copy local words.txt to HDFS:
hadoop dfs -copyFromLocal words.txt .


To submit wordcount in HDFS:
bin/hadoop jar wc.jar WordCount words.txt output

Check the output:
hadoop fs -cat output/part-r-00000
