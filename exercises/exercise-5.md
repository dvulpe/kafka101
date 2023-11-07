# Exercise 5 - reset consumer group offsets

Consume from the topic:

Describe the group:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:90992 --describe --group kafka101
```

Reset the consumer group to beginning:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --reset-offsets --group kafka101 --topic kafka101 --to-earliest --dry-run
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --reset-offsets --group kafka101 --topic kafka101 --to-earliest --execute
```

Consume from the topic should print numbers from 1-10:
```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --group kafka101 --topic kafka101 --timeout-ms 30000
````
