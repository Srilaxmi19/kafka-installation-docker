# kafka-installation-docker
# kafka-installation-docker

docker compose -f docker-compose.yml up -d
docker ps

docker exec -it <kafka_conatiner_id> /bin/sh
docker exec -it kafka /bin/sh

cd /opt
ls
cd kafka<version>
cd /opt/kafka_2.13-2.8.1
ls 
cd bin

Create Kafka topic
------------------
kafka-topics.sh --create --zookeeper zookeeper:2181 --replication-factor 1 --partitions 1 --topic quickstart

Start Producer app (CLI)
kafka-console-producer.sh --topic quickstart --bootstrap-server localhost:9092

Start consumer app (CLI)
kafka-console-consumer.sh --topic quickstart --from-beginning --bootstrap-server localhost:9092


