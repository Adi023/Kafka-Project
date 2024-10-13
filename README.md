# Kafka-Project
This project is trial version of kafka. Using this we communicate between delivery boy and consumer.

Kafka-Spring Boot Integration: Delivery Boy & End User Project

This repository contains two Spring Boot applications integrated with Kafka, each serving a different role in the delivery system:

delivery-boy branch: This branch contains the project for delivery personnel updates delivery status.

end-user branch: This branch contains the project for customers, allowing them to track delivery status.
Features

Delivery Boy
Kafka integration for receiving order assignments.
Real-time updates on delivery status via Kafka topics.
Spring Boot backend for managing delivery operations.

End User
Kafka integration for sending order requests.
Tracking delivery status in real-time via Kafka topics.
Spring Boot backend for order tracking.


Kafka Installation
This project requires a running Kafka instance to work. If you don't have Kafka installed, follow these steps:

Download Kafka: You can download Kafka from the official website at Kafka Downloads.

Set up Kafka: Follow the quickstart guide to set up Kafka and start the Zookeeper and Kafka server.

Project Setup
Clone the Repository
To start, clone the repository and switch to the desired branch.

bash
Copy code
# Clone the repository
git clone https://github.com/Adi023/Kafka-Project.git

# For delivery bot project
git checkout deliveryBoy

# For end user project
git checkout endUser
Install Dependencies
Make sure you have Java 17+ and Apache Kafka installed and running.

bash
Copy code
# Navigate into the project directory
cd Kafka-Project

# Install dependencies (for Maven)
mvn clean install
Configure Kafka Settings
Ensure that your Kafka settings (like bootstrap servers and topics) are properly configured in application.properties or application.yml in both branches.

Running the Application
Once your Kafka instance is running, you can start the Spring Boot application:

bash
Copy code
# Run Spring Boot application
mvn spring-boot:run
Branches
This repository has two primary branches:

delivery-boy: Code for delivery personnel.

end-user: Code for end users to place and track orders.

How Kafka Works in This Project
Kafka is used as the messaging broker between the delivery boy and end user systems. It facilitates real-time communication as follows:

End User places an order, which is published to a Kafka topic.
Delivery Boy listens to the topic and receives order assignments.
Delivery status updates are sent back to the End User via Kafka, providing real-time updates.
