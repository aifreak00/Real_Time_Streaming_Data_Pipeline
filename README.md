# 📊End-to-End Real Time Streaming Pipeline Project 🚀

Welcome to the **End-to-End Data Engineering Pipeline Project**! This guide will take you through the entire process of building a robust data pipeline, from data ingestion to processing and storage. We utilize a cutting-edge tech stack, including Apache Airflow, Python, Apache Kafka, Apache Zookeeper, Apache Spark, Cassandra, and Docker. Let's dive in! 🌊

## 🛠️ Tech Stack Overview

Here's a quick rundown of the technologies we'll be using:

- **Apache Airflow**: Orchestrates the pipeline and manages task scheduling.
- **Python**: The backbone of our scripting and automation.
- **Apache Kafka**: Handles real-time data streaming.
- **Apache Zookeeper**: Manages Kafka's distributed systems.
- **Apache Spark**: Processes large datasets efficiently.
- **Cassandra**: Stores the processed data for high availability and scalability.
- **PostgreSQL**: Temporary storage for fetched data.
- **Docker**: Containerizes all components for easy deployment and scalability.

## 🔍 Project Components

### 1. Data Source: Random User Data 📑
We use the [randomuser.me API](https://randomuser.me/) to generate random user data for our pipeline. This API provides a simple and effective way to simulate data ingestion.

### 2. Apache Airflow: Orchestration & Scheduling 🕹️
Apache Airflow is the heart of our pipeline, orchestrating various tasks. It fetches data from the randomuser.me API and stores it in a PostgreSQL database.

### 3. PostgreSQL: Intermediate Storage 🗄️
PostgreSQL acts as a temporary storage for the data fetched by Airflow, providing a reliable relational database solution.

### 4. Apache Kafka & Zookeeper: Real-time Data Streaming 📡
Kafka streams the data from PostgreSQL to the processing engine. Zookeeper ensures the stability and reliability of our Kafka clusters.

### 5. Control Center & Schema Registry: Monitoring & Management 👀
These tools help monitor Kafka streams and manage data schemas, ensuring smooth data flow and consistency.

### 6. Apache Spark: Data Processing Engine 🔥
Apache Spark processes the data with its distributed computing power, transforming and preparing it for storage.

### 7. Cassandra: Final Storage 📦
Cassandra stores the processed data, offering high availability and scalability for future analysis.

### 8. Docker: Containerization 🐳
All components are containerized using Docker, making deployment and scaling straightforward and efficient.

## 🚀 Getting Started

### Prerequisites

Ensure you have the following installed on your machine:
- Docker
- Docker Compose
- Python 3.8+
- Apache Airflow
- Apache Kafka
- Apache Zookeeper
- Apache Spark
- Cassandra
- PostgreSQL

### Installation & Setup

1. **Clone the Repository**
   ```bash
   git clone https://github.com/yourusername/data-engineering-pipeline.git
   cd data-engineering-pipeline
   ```

2. **Set Up Docker Containers**
   ```bash
   docker-compose up -d
   ```

3. **Initialize Apache Airflow**
   ```bash
   airflow db init
   airflow users create --username admin --password admin --firstname Admin --lastname User --role Admin --email admin@example.com
   ```

4. **Start the Airflow Scheduler and Webserver**
   ```bash
   airflow scheduler &
   airflow webserver
   ```

5. **Create Kafka Topics**
   ```bash
   kafka-topics.sh --create --topic user_data --bootstrap-server localhost:9092
   ```

6. **Launch the Pipeline**
   - Access the Airflow web UI at `http://localhost:8080`
   - Trigger the DAG to start the pipeline

## 📈 Monitoring & Management

- **Kafka Control Center**: Monitor your Kafka streams at `http://localhost:9021`
- **Airflow UI**: Manage your tasks and DAGs at `http://localhost:8080`
- **Spark UI**: Check the status of your Spark jobs at `http://localhost:4040`

## 📖 Documentation

For detailed documentation on each component, refer to the following:
- [Apache Airflow Documentation](https://airflow.apache.org/docs/)
- [Apache Kafka Documentation](https://kafka.apache.org/documentation/)
- [Apache Spark Documentation](https://spark.apache.org/docs/)
- [Cassandra Documentation](https://cassandra.apache.org/doc/latest/)
- [Docker Documentation](https://docs.docker.com/)

## 🏘️ Architecture/Workflows
![Data engineering architecture](https://github.com/aifreak00/Real_Time_Streaming_Data_Pipeline/assets/113664560/49774f11-c778-4d52-919b-e627d1b284eb)


