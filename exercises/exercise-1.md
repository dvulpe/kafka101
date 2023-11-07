# Exercise 1 - create topic

Start by listing topics

```bash
./kafka-topics.sh --bootstrap-server localhost:9092 --list
```

Create a topic with 1 partition:
```bash
./kafka-topics.sh --bootstrap-server localhost:9092 --create --topic kafka101 --partitions 1
```

Create a topic with 3 partitions:
```bash
./kafka-topics.sh --bootstrap-server localhost:9092 --create --topic kafka101-3 --partitions 3
```

Describe the topic:
```bash
./kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic kafka101
./kafka-topics.sh --bootstrap-server localhost:9092 --describe --topic kafka101-3
```

