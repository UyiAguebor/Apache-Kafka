# Consumers

- Consumers: read data from a topic - pull model
- Consumers automatically know wehicvh broker to read form
- In case of broker failures consumers know how to recover
- Data is read in order from low to high offset within each partitions

## Consumer Deserializer

Deserialize indicates how to transform bytes into objects/data
They are used on the value and the key of the message