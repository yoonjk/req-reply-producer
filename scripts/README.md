
## kafka 

```bash
docker run --rm -p 2181:2181 -p 3030:3030 -p 8081-8083:8081-8083 -p 9581-9585:9581-9585 -p 9092:9092 -e ADV_HOST=127.0.0.1 landoop/fast-data-dev:latest
```

## kafka ui

```bash
docker run --rm -it -p 8000:8000 -e "KAFKA_REST_PROXY_URL=http://localhost:8082"  landoop/kafka-topics-ui
```

## kafka request/reply
```
kafka-topics --bootstrap-server localhost:9092 --topic requestreply-topic --partitions 2 --alter
```