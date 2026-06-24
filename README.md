# JournalAppln

# JournalAppn

A secure, event-driven personal journaling platform built using the Spring Boot ecosystem. This project goes beyond basic CRUD functionality by implementing decentralized security and asynchronous, message-driven architecture.

## 🚀 Key Features
- **Full CRUD Management:** Seamlessly create, read, update, and delete journal entries.
- **Secure Authentication:** Integrated **OAuth2** for secure user login and token-based authorization.
- **Event-Driven Architecture:** Utilizing **Apache Kafka** to handle asynchronous tasks (e.g., activity logging, notifications, or analytics processing) ensuring high throughput and decoupling.

## 🛠️ Tech Stack
- **Backend Framework:** Java / Spring Boot (Spring Security, Spring Web)
- **Message Broker:** Apache Kafka
- **Security:** OAuth2 / JWT
- **Database:** [e.g., PostgreSQL / MySQL / MongoDB - Fill this in!]
- **Build Tool:** [Maven / Gradle]

## 🏗️ System Architecture
The application decouples core journaling actions from background processing using a publisher-subscriber model:
1. **User Auth:** Authenticates via the OAuth2 provider.
2. **Journal Service:** Handles HTTP requests and produces event messages to Kafka topics upon journal updates.
3. **Consumer Service:** Asynchronously processes Kafka event streams for audit logs or background triggers.
