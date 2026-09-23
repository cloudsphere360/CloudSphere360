# CloudSphere360 Portfolio

A Java + Maven portfolio website starter project for CI/CD practice.

## Goals
- Personal portfolio
- Blog
- Projects
- Contact/business presence
- Java + Maven CI practice

## Current phase
Phase 1 focuses on Java + Maven + tests and a simple runnable web application.
CI/CD files such as Jenkinsfile are intentionally NOT included so you can build the pipeline from scratch.

## Prerequisites
- JDK 21+
- Maven 3.9+
- Git

## Build
```bash
mvn clean package
```

## Run
```bash
mvn spring-boot:run
```

Open http://localhost:8080

## Project structure
- `src/main/java` - application code
- `src/main/resources` - templates/static resources
- `src/test/java` - tests
- `pom.xml` - Maven configuration

Later phases can add Docker, Jenkins, security scanning, registry, deployment GitOps, and Kubernetes.
