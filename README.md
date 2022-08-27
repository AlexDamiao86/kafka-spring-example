# Getting Started

## Start Kafka Broker 

~~~bash
docker compose up -d
~~~

## Create topic 

~~~bash
docker compose exec broker \
  kafka-topics --create \
    --topic purchases \
    --bootstrap-server localhost:9092 \
    --replication-factor 1 \
    --partitions 1
~~~

## Build project 

You can compile the code before preceding by with:

~~~bash
gradle build
~~~

## Consume events

Run the following command to run the Spring Boot application for the Consumer.

~~~bash
gradle bootRun --args='--consumer'
~~~

## Produce events 

Run the following command to run the Spring Boot application for the Producer.

~~~bash
gradle bootRun --args='--producer'
~~~

