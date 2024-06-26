# Angular + Node.js

This project demonstrates both client-side component rendering and hydration with Angular, as well as server-side rendering with Node.js and Socket.IO for real-time communication. It also includes Docker configurations for easy deployment.

## NOTE

This sample showcases how you could deploy a full-stack application with Angular and Node.js using Defnag. The Docker setup ensures the app can be easily built and deployed. However, for production use cases, make sure to use appropriate database and security configurations.

## Essential Setup Files

1. Download [Defang CLI](https://github.com/defang-io/defang)
2. (Optional) If you are using [Defang BYOC](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) authenticated with your AWS account
3. (Optional for local development) [Docker CLI](https://docs.docker.com/engine/install/)

## Prerequisites

1. Download [Defang CLI](https://github.com/defang-io/defang)
2. (Optional) If you are using [Defang BYOC](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-configure.html) make sure you have properly authenticated your AWS account
3. [Node.js](https://nodejs.org/en/download/package-manager/)
4. [Angular CLI](https://angular.io/cli)

## Development

For development, we use a local container. This can be seen in the Dockerfile and docker-compose.yml files where we statically served the Angular frontend onto the Node.js backend. To run the sample locally after cloning the repository, you can run on Docker by doing:

1. `docker-compose up --build`

## A Step-by-Step Guide

1. Open the terminal and type `defang login`
2. Type `defang compose up` in the CLI
3. Your app should be up and running with Defang in minutes!

---

Title: Angular + Node.js

Short Description: A full-stack application using Angular for the frontend and Node.js with Socket.IO for the backend, containerized with Docker.

Tags: angular, nodejs, Socket.IO

Languages: typescript, javascript
