# Exercise 4 - consumer group

Consume from the topic:

```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic kafka101 --group kafka101 --from-beginning --timeout-ms 30000
```

Describe the group:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --group kafka101
```


