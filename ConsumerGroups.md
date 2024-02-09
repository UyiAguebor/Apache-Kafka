# Consumer Groups

All the consumers in an application read data as a consumer groups
Each consumer within a group reads from exclusive partitions

## What if too many consumers?

If you have more consuymers than partitions some consumers will be inactive

## Multiple consumers on one topic

In Apache Kafka it is acceptable to have multiple consumer groups on the same topic

## Consumer Offsets

Kafka stores the offsets at which ca consumer group has been read
The offsets committed are in Kafka topic named _-consumer_ofdfsets
After Consumer group has processed data received from Kafka it should be periodically committing the offsets
if a consumer dies it will be able to read back from where it left off thanks to the commited consumer offsets

## Delivery semantics for consumers

By default, Java consumers will automatically commit offsets at least once
There are 3 Delivery semantics if you choose to commit manually
- At least once (offsets commited after msg processed)
- At most once (commited as soon as messages recieved)
- Exactly once ()