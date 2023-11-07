# Exercise 4 - consumer group

Consume from the topic:

```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic kafka101 --group kafka101 --from-beginning
```

Describe the group:
```bash
./kafka-ocnsumer-groups --bootstrap-server localhost:90992 --describe --group kafka101
```


