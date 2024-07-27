# apache-kafka-spring-boot-demo-app
Demo app with Apache Kafka and Spring Boot


Show topic list:

```
docker exec -it kafka-learn kafka-topics --list --bootstrap-server localhost:9092
```

Send message to topic:

```
docker exec -it kafka-learn bash -c "echo 'New message' | kafka-console-producer --topic learn-topic --bootstrap-server localhost:9092";
```


Consume message from topic:

```
docker exec -it kafka-learn kafka-console-consumer --topic learn-topic --bootstrap-server localhost:9092 --from-beginning
```
