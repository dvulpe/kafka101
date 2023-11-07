# Exercise 3 - consumer

Consume from the topic:

```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic kafka101 --timeout-ms 30000
```

We expect to see the numbers from 1 to 10 printed, but nothing is returned, let's investigate why.

List the consumer groups

```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --list
```

Can you spot the reason why the console consumer doesn't show the messages?
