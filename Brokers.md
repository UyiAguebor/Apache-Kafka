# Kafka Brokers

A Kafka cluster is composed of multiple brokers (servers)
Each broker is identified with its ID (integer)
Each broker contains certain topic partitions
After connecting to any broker you will be connected to the entire cluster 
A good number to get started is 3 brokers but some big clusters have over 100 brokers
In these examples we choose to number brokers starting at 100 (arbitrary)

## Brokers and topics

Topic-A -> 3 partitions
Topic-B -> 2 partitions

broker 1 -> topic a partition 0 & topic b partition 1  etc...

## Kafka Broker Discovery

Every kafka broker is also called a bootstrap server
You only need to connect to one broker and the Kafka clients will know hwo to be connected to the enitre cluster