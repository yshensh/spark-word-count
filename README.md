## Maven Build 
mvn clean
mvn compile
mvn package

## Run

### Intellij
Import the project and configure `Run` => `Edit Configurations` as the following:
```
Main Class: WordCount
VM Options: -Dspark.master=local
Program Parameters: <input file path> <output file path>
```

Note: Please make sure you uncomment `<scope>provided</scope>` in the following section of `pom.xml`

```
        <dependency>
            <groupId>org.apache.spark</groupId>
            <artifactId>spark-core_2.10</artifactId>
            <version>2.0.0</version>
            <scope>provided</scope>
        </dependency>
```

### Build JAR

Compile and Build JAR with Maven
```
mvn validate && mvn compile && mvn package
````

Launch Application on Local Host
```
$SPARK_HOME/bin/spark-submit --master local --class WordCount ./target/spark-word-count-0.1.0-SNAPSHOT.jar ../inputFile ./outputFile
```
Please reference [Spark Submitting Applications](http://spark.apache.org/docs/latest/submitting-applications.html) for more details

