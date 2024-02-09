# Topics

Topics: a particular stream of data

- Like a s table in a database
- You can have as many topics as you want 
- A topic is identified by its name
- Any kind of message format
- The sequence of messages is called a data stream

## Topics are split in partitions

- Messages within each partition are ordered
- Each message within a partition gets an incremental id, called offset.
- Offset only have a meaning for a specific partition
- Order is guaranteed only within a partition
- data is assigned randomly to a partition unless a key is provided
- you can have as many partitions per topic as you want.

## Topics are immutable

- once data is written to a partition, it cannot be changed.

## Data is only kept for a limited time

- default is one week (configurable)

