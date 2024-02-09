# Topic Replication Factor

Topics should have a replication factor > 1 usually between 2 & 3
This way if a broker is down another broker can serve the data

## Concept of Leader for a Partition

- At anytime only one broker can be a leader for a given partition
- Producers can only send data to the broker that is leader of a partition
- The other brokers will replicate the data
- Therefore each partition has one leader and multiuple IRS (in-sync replica)