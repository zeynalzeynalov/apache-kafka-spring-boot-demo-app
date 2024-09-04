# apache-kafka-spring-boot-demo-app
Demo app with Apache Kafka and Spring Boot

Starting Kafka and Zookeeper docker containers:

```
docker-compose up -d
```


### Showing the topic list:

```
docker exec -it kafka-learn kafka-topics --list --bootstrap-server localhost:9092
```

### Sending the message to the topic:

```
docker exec -it kafka-learn bash -c "echo 'New message' | kafka-console-producer --topic learn-topic --bootstrap-server localhost:9092";
```


### Consuming the message from the topic:

```
docker exec -it kafka-learn kafka-console-consumer --topic learn-topic --bootstrap-server localhost:9092 --from-beginning
```
