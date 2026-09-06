# Containerized Microservices Voting Application

A multi-service voting application used to explore containerization, service-to-service communication, and local orchestration with Docker Compose.

## Architecture

```text
Vote Service (Python / Flask)
          │
          ▼
        Redis
          │
          ▼
Worker Service (.NET)
          │
          ▼
      PostgreSQL
          │
          ▼
Result Service (Node.js / Express)
```

## What This Project Demonstrates

- Running multiple application services as containers
- Building Docker images for different technology stacks
- Connecting services through Docker networking
- Using Redis for queued vote messages
- Processing messages with a .NET worker
- Persisting results in PostgreSQL
- Serving results through a Node.js/Express application
- Orchestrating the complete stack with Docker Compose

## Technology Stack

| Component | Technology |
| --- | --- |
| Vote service | Python / Flask |
| Message queue | Redis |
| Worker | .NET |
| Database | PostgreSQL |
| Result service | Node.js / Express |
| Containerization | Docker |
| Orchestration | Docker Compose |

## Running the Application

The easiest way to start the complete stack is:

```bash
docker compose up --build
```

The Compose configuration starts the application services together with Redis and PostgreSQL and provides the networking required for service-to-service communication.

## Project Structure

```text
vote/               Python voting service
worker/             .NET background worker
result/             Node.js results service
docker-compose.yml  Multi-container orchestration
```

## Purpose

This project focuses on the DevOps side of a distributed application: containerization, networking, service dependencies, and repeatable local environments.

It is intentionally a small application so the infrastructure and deployment concepts remain easy to understand.

## Status

Completed containerization and microservices project.
