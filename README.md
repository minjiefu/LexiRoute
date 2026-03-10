# Lexiroute: Serverless Graph Routing Bot

**Lexiroute** is an end-to-end, cloud-native conversational AI designed to analyze network topologies and resolve shortest-path queries between nodes in a directed graph.

## 🚀 Project Overview
This project leverages a **Serverless Architecture** to provide a scalable and cost-effective routing service. Users can interact with the bot through a web interface to query the distance (steps) between cities/nodes, with backend logic powered by BFS (Breadth-First Search).

## 🛠 Tech Stack
* **Conversational AI:** AWS Lex V2
* **Compute:** AWS Lambda (Python 3.x)
* **Database:** Amazon DynamoDB (NoSQL)
* **Security:** AWS Cognito & IAM
* **Hosting:** Amazon S3 (Static Website)
* **Development:** Boto3, Python Requests

## 📐 Architecture
1.  **Ingestion:** A Python script sends graph data (nodes/edges) to the backend.
2.  **Logic:** AWS Lambda executes a **BFS algorithm** to pre-calculate the shortest paths between all node pairs.
3.  **Storage:** Results are stored in **DynamoDB** for sub-millisecond query performance.
4.  **Interaction:** Users query distances via a web-based chat UI connected to **AWS Lex**.
5.  **Authentication:** **AWS Cognito** secures guest access to the Lex bot.

## 📖 Features
* **Natural Language Processing:** Understands queries like "How far is it from Chicago to Urbana?"
* **Graph Intelligence:** Supports complex directed graphs with edge weights of 1.
* **Instant Response:** Pre-calculated routing tables ensure immediate feedback without redundant calculations.

