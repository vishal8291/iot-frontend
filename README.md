# IoT Dashboard Backend - FastAPI

This is a production-ready FastAPI service that listens to real-time sensor data over MQTT, processes incoming JSON messages, and generates alerts based on predefined thresholds.

Key Features
* **MQTT Subscription**: Subscribes to 10 MQTT topics (sensor/topic1 to sensor/topic10).
* **Real-time Processing**: Validates JSON messages containing Temperature, Humidity, Voltage, Current, and Pressure.
* **Threshold Validation**: Automatically generates alerts if values exceed set limits (e.g., Temp > 50.0°C).
* **Database Management**: Stores raw sensor data and alert metadata (timestamp, violated keys, actual values) in MySQL.
* **Containerization**: Fully Dockerized for easy deployment.

Tech Stack
* **Framework**: FastAPI (Python)
* **Database**: MySQL
* **Broker**: Mosquitto MQTT
* **Libraries**: SQLAlchemy (ORM), Paho-MQTT (Listener)
  
Hosting Exploration
As per the task requirements, I explored hosting this backend on **AWS EC2** using Docker Compose. For production-grade MQTT, a managed broker like **HiveMQ** would be used for high availability.
