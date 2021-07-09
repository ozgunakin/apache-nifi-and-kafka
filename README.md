# Apache Nifi and Kafka Integration

This project includes a simple pipeline example to be used to establish a connection between Apache Nifi and Apache Kafka.

## Architecture

![](.gitbook/assets/image%20%283%29.png)

## Pipeline 1 : Nifi to Kafka

We will use GenerateFlowfiles to generate dummy data, and PublishKafka processor to send this dummy data to Kafka broker.

![](.gitbook/assets/image%20%284%29.png)

* [x] You need to configure PublishKafka processor according to your broker address and topic name.

![](.gitbook/assets/image%20%285%29.png)

## Pipeline 2 : Kafka to Nifi

We will use ConsumeKafka processor to consume the data from Kafka using Nifi.

* [x] Please select ConsumeKafka Processor

![](.gitbook/assets/image%20%281%29.png)

![](.gitbook/assets/image%20%282%29.png)

## Start Data Flow

Start all processors you configured. If pipelines are properly configured, you should be able to see all published data produced from the first pipeline will be consumed by the second pipeline.

![](.gitbook/assets/image%20%287%29.png)

