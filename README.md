# Real-Time-IoT-Dashboard-with-AWS-IoT-Core-Timestream-and-Grafana

---

# IoT Data-to-Dashboard Solution

This project demonstrates how to create a scalable and secure IoT data pipeline using **AWS IoT Core**, **Amazon Timestream**, and **Amazon Managed Grafana**. It covers the end-to-end process from collecting IoT device telemetry data to visualizing it on a real-time dashboard.

---

## Features

1. **IoT Device Simulation**: 
   - A virtual IoT device (your laptop) sends telemetry data using the AWS IoT Python SDK.
   
2. **Data Storage**:
   - Collected telemetry data is stored in **Amazon Timestream**, a purpose-built time-series database.

3. **Data Visualization**:
   - Data is visualized in **Amazon Managed Grafana**, creating real-time dashboards for insights.

---

## Prerequisites

Before starting, ensure you have:
- **Python Installed**: The virtual IoT device runs Python scripts.
- **AWS Account**: Access to AWS IoT Core, Amazon Timestream, and Grafana services.
- **Basic Knowledge**: Familiarity with AWS services and Python programming.

---

## Steps to Set Up the Solution

### 1. Create an IoT Device in AWS IoT Core
- Set up an AWS IoT Thing in the AWS IoT Core console.
- Download the connection kit with certificates and keys.
- Use the provided `pubsub.py` script to send JSON-formatted telemetry data.

### 2. Store Data in Amazon Timestream
- Create a Timestream database and table in the AWS Console.
- Configure an AWS IoT Core Rule to route incoming telemetry data to Timestream.

### 3. Visualize Data in Grafana
- Set up a managed Grafana workspace in AWS.
- Connect the Timestream database as a data source.
- Create real-time dashboards and panels to visualize the data.

---

## How It Works
1. **Data Collection**:
   - The IoT device sends telemetry data (e.g., CPU utilization) in JSON format via MQTT to AWS IoT Core.
2. **Data Routing**:
   - An IoT Rule filters and routes this data to Amazon Timestream for storage.
3. **Visualization**:
   - Grafana pulls data from Timestream and displays it on a dashboard.

---

## Project Structure
- **AWS IoT Core**: Collects and routes IoT telemetry data.
- **Amazon Timestream**: Stores the time-series data securely.
- **Amazon Managed Grafana**: Visualizes data on interactive dashboards.

---

## Additional Resources

- [AWS IoT Core Documentation](https://docs.aws.amazon.com/iot/latest/developerguide/what-is-aws-iot.html)
- [Amazon Timestream Documentation](https://docs.aws.amazon.com/timestream/latest/developerguide/what-is-timestream.html)
- [Amazon Managed Grafana Documentation](https://docs.aws.amazon.com/grafana/latest/userguide/what-is-grafana.html)
