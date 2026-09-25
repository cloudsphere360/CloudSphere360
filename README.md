# CloudSphere360

CloudSphere360 is a DevOps project demonstrating a modern CI/CD and GitOps-based application deployment workflow.

## CI/CD Architecture

<p align="center">
  <img src="./docs/architecture/ci-cd-architecture.gif"
       alt="CloudSphere360 CI/CD Architecture"
       width="100%">
</p>

### Architecture Overview

The project follows a CI/CD and GitOps-based approach:

- **GitHub** – Source code management
- **Jenkins** – Continuous Integration and build automation
- **Maven** – Java application build
- **Docker** – Application containerization
- **Docker Hub** – Container image registry
- **GitOps Repository** – Kubernetes deployment configuration
- **Argo CD** – Continuous Deployment
- **AWS EKS / Kubernetes** – Application runtime

### CI Flow

```text
Developer → GitHub → Jenkins → Maven → Docker Build → Docker Hub

### CD Flow

```text
Docker Hub → GitOps Repository → Argo CD → AWS EKS / Kubernetes