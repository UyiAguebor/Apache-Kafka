# Producers

Producers write data to topics
Producers know to which partition to write to and which kafka broker (server) has it.
In case of kafka broker failures producers will automaticallyt recover

## Producers: Message Keys

Producers can choose to send a key with the message.
if key is null data is sent round robin.
if key isnt null then all messages for that key will go alays to the same partition.
A key are typiucally sent if youy need messages ordering ifor a specific field.

## Kafka Messages anatomy

- Key binary (can be null)
- Value binary (can be null)
- Compressioon Type
- Headers (optional)
- Timestamp

## Kafka Message Serializer

transform your data / objects into bytes

key object:123 (int) -> Keyserializer=IntegerSerializer (bytes)-> Key Binary

## Producer Acknowledgments (acks)

producers can choose to receive acknowledgement of data writes

acks=0: wont wait for acknowledgement (possible data loss)
acks=1: produicers will wait for leader acknowledgment ( limited data loss)
acks=all: Leader + replicas acknowledgement (no data loss)