# Kafka 101

The stack can be brought up with `docker-compose`.
It uses:
* zookeeper
* 3 kafka brokers (spread across 3 racks)

### Start the Kafka stack

```bash
docker-compose pull
docker-compose up -d
```
Check the stack is started by running 
```bash
docker ps
```
You should see the following containers:
```bash
CONTAINER ID   IMAGE                             COMMAND                  CREATED         STATUS         PORTS                                                                 NAMES
ee5d03c0cf3d   confluentinc/cp-kafka:7.5.1       "/etc/confluent/dock…"   7 minutes ago   Up 7 minutes   0.0.0.0:9092->9092/tcp                                                kafka-0
d7b468504864   confluentinc/cp-kafka:7.5.1       "/etc/confluent/dock…"   7 minutes ago   Up 7 minutes   9092/tcp, 0.0.0.0:9093->9093/tcp                                      kafka-1
bf1aad0fab20   confluentinc/cp-kafka:7.5.1       "/etc/confluent/dock…"   7 minutes ago   Up 7 minutes   9092/tcp, 0.0.0.0:9094->9094/tcp                                      kafka-2
0760fa0e005c   confluentinc/cp-zookeeper:7.5.1   "/etc/confluent/dock…"   7 minutes ago   Up 7 minutes   2888/tcp, 0.0.0.0:2181->2181/tcp, 3888/tcp, 0.0.0.0:15555->5555/tcp   zookeeper
```

### Download Apache Kafka 

Go to https://kafka.apache.org/downloads and choose the binary download with Scala 2.13,
or run the following command:
```bash
curl -fsSL -o kafka.tgz https://downloads.apache.org/kafka/3.6.0/kafka_2.13-3.6.0.tgz
```
Unpack the archive locally:
```bash
tar -zxvf kafka.tgz
```
