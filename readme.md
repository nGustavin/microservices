## 1. Running Kafka container
```bash
cd ./kafka && docker-compose up -d
```

## 2. Creating Topic to store events
```bash
docker compose exec broker \
  kafka-topics --create \
    --topic purchases \
    --bootstrap-server localhost:9092 \
    --replication-factor 1 \
    --partitions 1
```