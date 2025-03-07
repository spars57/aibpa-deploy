# Techinal Specification

## Overview

This project focuses on developing an intelligent personal assistant using a multi-agent AI system. The goal is to create a solution capable of managing tasks, answering queries, scheduling events, and automating workflows efficiently. Unlike traditional assistants, this system employs multiple collaborative AI agents to achieve better results.

The requirements for this project are the following:

- AI & NLP: OpenAI API (or fine-tuned LLM), spaCy, Rasa, LangChain
- Multi-Agent Frameworks: JADE, SPADE, or a custom Python-based MAS
- Backend: Flask/Django (for API and agent communication)
- Frontend: React.js (for user interface)
- Database: PostgreSQL/MongoDB (to store user preferences and task logs)
- DevOps: Docker, Kubernetes (for scalable deployment)

# Architecture

## Backend

Backend will consist of a REST API which will be used by the frontend to communicate with the backend.

### Technologies

For the development of this service, [Python 3.10](https://www.python.org/downloads/) and [Flask 3.1.x](https://flask.palletsprojects.com/en/stable/installation/) will be used as it is a requirement for the project.

For database management [SQLAlchemy](https://www.sqlalchemy.org/) will be used, this library allows to generate models from database schema, and also provides a way to interact with the database using ORM.

For AI we will use [OpenAI](https://openai.com/) API, this API will be used to generate responses to the user queries.

For testing [Pytest](https://docs.pytest.org/en/stable/) will be used, this library provides a way to test the application from the developer perspective.

### Database

For database [PostgreSQL](https://www.postgresql.org/) will be used, a set of constraints will be defined to ensure the data integrity. The database will be deployed on [AWS Relational Database Service](https://aws.amazon.com/rds/) and will use [Flyway](https://flywaydb.org/) to manage the migrations.

### Authentication

For authentication [JWT](https://jwt.io/) will be used, this is a standard way to authenticate and authorize users in a web application. The token will be sent in the Authorization header of every request. This process should be handled by an interceptor in REST API which should return [HTTP 401](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/401) if the token is invalid or expired.

### Security

For security all sensitive data will be stored in the git repository as environment variables. This includes sensitive information like API keys, database credentials, etc.

## Frontend

Frontend will consist on a [ReactJS 18](https://react.dev/) application written in [TypeScript](https://www.typescriptlang.org/).

### Technologies:

As mentioned before, the frontend will be written in [TypeScript](https://www.typescriptlang.org/) and will use [ReactJS 18].

For state management [React Redux Toolkit](https://redux-toolkit.js.org/) will be used, to ensure large scale scalability and maintainability of the application.

For asyncronous application [React Query](https://tanstack.com/query/latest/docs/framework/react/react-native) will be used, this library provides a way to manage the state of asyncronous operations.

For routing [React Router](https://reactrouter.com/) will be used, this library provides a way to manage the routes of the application.

For styling [Material UI](https://mui.com/) will be used, this library provides a way to manage the styling of the application.

For dependency management [Yarn](https://yarnpkg.com/) will be used, this is a package manager for JavaScript and TypeScript.

For building the application [Vite](https://vitejs.dev/) will be used, this is a build tool for JavaScript and TypeScript.

### E2E Testing

For E2E testing [Playwright](https://playwright.dev/) will be used, this library provides a way to test the application from the user perspective.

## Deployment

There will be 2 docker images, one for frontend and one for backend.
A docker compose file will include the services for frontend and backend and will be used to run the application.

For deployment [Kubernetes](https://kubernetes.io/) will be used, this is a container orchestration tool that will be used to deploy the application which contains a out of the box load balancer, service discovery and a way to manage the secrets.
