1. start the kafka broker
docker-compose up -d

2. create a topic
#quickstart is the topic name
docker exec broker \
kafka-topics --bootstrap-server broker:9092 \
             --create \
             --topic quickstart

docker exec broker kafka-topics --bootstrap-server broker:9092 --create --topic quickstart 

3. Read the message
docker exec --interactive --tty broker \
kafka-console-consumer --bootstrap-server broker:9092 \
                       --topic quickstart \
                       --from-beginning


docker exec --interactive --tty broker kafka-console-consumer --bootstrap-server broker:9092 --topic robertramirez --from-beginning

4. Write some messages
docker exec --interactive --tty broker \
kafka-console-producer --bootstrap-server broker:9092 \
                       --topic quickstart

docker exec --interactive --tty broker kafka-console-producer --bootstrap-server broker:9092 --topic robertramirez 
