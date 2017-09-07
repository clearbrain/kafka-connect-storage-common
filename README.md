# Kafka Connect Common Modules for Storage Connectors
Shared software modules among [Kafka Connectors](http://kafka.apache.org/documentation.html#connect) that target distributed filesystems and cloud storage.

*This is a fork of the Confluent repo to add the functionality into the FieldPartitioner to allow for multifield partitioning*
*Deployment Steps*
1. Ensure that you have maven installed on your computer
2. Run `mvn package`.  This will build the jars
3. Copy the file `package-kafka-connect-storage-common/target/kafka-connect-storage-common-package-4.0.0-SNAPSHOT-package/share/java/kafka-connect-storage-common/kafka-connect-storage-partitioner-4.0.0-SNAPSHOT.jar` to the kafka cluster under `/home/ec2-user/confluent-3.3.0/share/java/kafka-connect-storage-common`.  You can use scp or any ftp tool (make sure that it doesn't get copied as 0 bytes).  Make sure to move/remove any existing jar under the target directory that has a name prefixed with `kafka-connect-storage-partitioner` (we are trying to overwrite the file).

# Development

To build a development version you'll need a recent version of Kafka. You can build
*kafka-connect-storage-common* with Maven using the standard lifecycle phases.


# Contribute

- Source Code: https://github.com/confluentinc/kafka-connect-storage-common
- Issue Tracker: https://github.com/confluentinc/kafka-connect-storage-common/issues


# License

The project is licensed under the Apache 2 license.
