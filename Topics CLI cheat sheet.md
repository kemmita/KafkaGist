0. This takes place inside of a Ubuntu shell using the Kafka Binaries, navigate to kafka shell files, for docker -> /opt/bitnami/kafka/bin
1. Create topic.
```sh
kafka-topics.sh --create --topic my_test_topic --bootstrap-server localhost:9092 --partitions 3 --replication-factor 1
```
2. List topics
```sh
kafka-topics.sh --list --bootstrap-server localhost:9092
```
3. Create producer to write to topic
```sh
kafka-console-producer.sh --broker-list localhost:9092 --topic my_test_topic
```
4. Create consumer to read from topic
```sh
kafka-console-consumer.sh --bootstrap-server localhost:9092 --topic my_test_topic --from-beginning
```
