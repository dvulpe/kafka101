# Exercise 5 - reset consumer group offsets

Consume from the topic:

Describe the group:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:90992 --describe --group kafka101
```

Reset the consumer group to beginning:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --reset-offsets --topic kafka101 --to-earliest

Consume from the topic should print numbers from 1-100:
```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --group kafka101 --topic kafka101 --property print.offset=true
````
