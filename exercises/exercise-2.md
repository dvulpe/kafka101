# Exercise 2 - producer

Ensure the topic exists:
```bash
    ./kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic kafka101
```

Write the integers from 1-10 to the `kafka101` topic:

```bash
seq 1 10 | ./kafka-console-producer.sh --bootstrap-server localhost:9092 --topic kafka101
```

