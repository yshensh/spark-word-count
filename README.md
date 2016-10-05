## Maven Build 
mvn clean
mvn compile
mvn package

## Run
```
/usr/local/Cellar/apache-spark/1.6.1/bin/spark-submit --master local --class WordCount.class ./target/spark-word-count-0.1.0-SNAPSHOT.jar ../inputFile ./outputFile
```
Please reference [Spark Submitting Applications](http://spark.apache.org/docs/latest/submitting-applications.html) for more details

##TODO
- Understand Maven build uber JAR