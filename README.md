# Realtime Data Streaming | End-to-End Data Engineering Project

## Introduction 
This project employs a multifaceted technological stack to establish an end-to-end data processing pipeline. The workflow commences by fetching data from the `randomuser.me` API to generate synthetic user data. This raw data is subsequently channeled through **Apache Airflow** for data orchestration and storage in a **PostgreSQL** database. 

The data is then streamed through **Apache Kafka** in conjunction with **Apache Zookeeper** to facilitate real-time data movement from PostgreSQL to the processing engine. For streamlined management and monitoring of Kafka streams, **Control Center** and **Schema Registry** are employed to handle schema configurations and ensure effective oversight of the data streams.

Subsequently, **Apache Spark** is utilized to conduct data processing tasks, following which the processed data is persisted in a **Cassandra** database, providing a durable storage solution for the refined information.

The entire pipeline is encapsulated within **Docker** containers, affording a streamlined and portable deployment mechanism. 

## System Architecture

![System Architecture](https://github.com/korikana037/realtime-data-streaming/blob/main/Data%20engineering%20architecture.png)

The project is designed with the following components:
- **Data Source**:  `randomuser.me` API is used to generate random user data for the pipeline.
- **Apache Airflow**: Helps with orchestrating the pipeline and storing fetched data in a PostgreSQL database.
- **Apache Kafka and Zookeeper**: Used for streaming data from PostgreSQL to the processing engine.
- **Control Center and Schema Registry**: Helps in monitoring and schema management of the Kafka streams.
- **Apache Spark**: Responsible for data processing with master and worker nodes.
- **Cassandra**: Database to store the processed data.
- **Docker**: Containerize the entire pipeline.

## Technologies Used

- Apache Airflow
- Python
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL
- Docker


## summary
Here’s a summary of the project’s key components and workflow:

1. Data Ingestion: The project begins with data ingestion, using the randomuser.me API to generate synthetic user data. Apache Airflow orchestrates this process, managing data ingestion and storing it initially in a PostgreSQL database.

2. Data Streaming with Kafka: The real-time streaming component uses Apache Kafka, a distributed streaming platform, to move data from PostgreSQL into the data processing engine. Kafka is paired with Apache Zookeeper for managing Kafka's distributed environment, handling configurations, and ensuring consistent data flow.

3. Data Processing with Spark: Apache Spark, a powerful data processing engine, performs data transformations and aggregations. Spark's distributed setup with master and worker nodes enables efficient data processing on large datasets in real-time.

4. Storage and Querying: Processed data is stored in Cassandra, a NoSQL database designed for high availability and performance. This setup allows for both scalable data storage and querying.

5. Containerization with Docker: The entire pipeline is containerized using Docker, which simplifies deployment and ensures consistency across different environments, making the setup portable and easy to replicate.

## Acknowledgements
I would like to thank [Yusuf Ganiyu](https://www.linkedin.com/in/yusuf-ganiyu-b90140107/) for this amazing project. 


Please follow the tutorial here to build this data engineering pipeline yourself.
[YouTube Video Tutorial](https://www.youtube.com/watch?v=GqAcTrqKcrY)
