# Exercise 6 - delete records

Consume from the topic:

Describe the group:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --describe --group kafka101
```

Reset the consumer group to beginning:
```bash
./kafka-consumer-groups.sh --bootstrap-server localhost:9092 --reset-offsets --group kafka101 --topic kafka101 --to-earliest --execute
```

Consume from the topic should print numbers from 1-10:
```bash
./kafka-console-consumer.sh --bootstrap-server localhost:9092 --group kafka101 --topic kafka101 --property print.offset=true --timeout-ms 30000
````

Create a json file describing the offsets:
```
cat <<EOF>offsets.json
{ 
  "partitions": [
    {"topic": "kafka101", "partition": 0, "offset": 6 }
  ]
}
EOF
```

Delete message at offset:
```bash
./kafka-delete-records.sh --bootstrap-server localhost:9092 --offset-json-file offsets.json
```

Reset the consumer group to beginning and consume from the beginning.
