# Spring Boot Demo

This repository contains a simple demo Spring Boot application generated using [Spring Initializr](https://start.spring.io/).

## Features

- Basic Spring Boot application structure
- Provided `Dockerfile` for containerization
- GitHub Actions workflow for CI and Docker image publishing

## Docker Image

A `Dockerfile` is included to build a Docker image from the generated application JAR.

Published images are available on Docker Hub:  
[makram89/spring-demo](https://hub.docker.com/r/makram89/spring-demo)

## GitHub Actions Workflow

The repository contains a GitHub Actions workflow which:

- Builds and packages the application with Maven
- Builds the Docker image
- Pushes the Docker image to Docker Hub automatically

### Workflow Triggers

| Trigger                         | Description                                                        | Docker Tags Example                              |
|----------------------------------|---------------------------------------------------------------------|--------------------------------------------------|
| Push of a new Git tag (e.g. `v1.0.0`) | Builds & pushes image; tag from the Git reference (e.g. `v1.0.0`)   | `makram89/spring-demo:v1.0.0`, `:latest`         |
| Manual trigger (workflow_dispatch)    | Allows manual image build & publishing (uses branch name as tag)    | `makram89/spring-demo:main`, `:latest`           |

## Quick Links

- [Spring Initializr](https://start.spring.io/)
- [Docker Hub: makram89/spring-demo](https://hub.docker.com/r/makram89/spring-demo)

---

Feel free to open issues or submit pull requests for improvements or suggestions!
