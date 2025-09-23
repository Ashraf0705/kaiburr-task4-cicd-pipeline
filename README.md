# Kaiburr Technical Assessment - Task 4: CI/CD Pipeline

This repository contains the solution for **Task 4**, an automated CI/CD pipeline built with **GitHub Actions**.

The purpose of this pipeline is to automate the build, testing, and containerization process for the Java Spring Boot application developed in Task 1.

---

## 🚀 Pipeline Architecture

This pipeline is designed as a standalone workflow that operates on a separate application repository, a common pattern for managing deployments.

- **Trigger:** The workflow is triggered manually (`workflow_dispatch`), allowing for controlled deployments.
- **Source Repository:** It checks out the source code from the `kaiburr-task1-java-api` repository.
- **CI (Continuous Integration):** It compiles and packages the Java application using Maven, ensuring the code is in a buildable state.
- **CD (Continuous Deployment):** It builds a Docker image from the application's `Dockerfile` and pushes the resulting image to a public Docker Hub repository.

---

## 🛠️ Workflow Steps

The pipeline consists of a single job with the following key steps:

1.  **Checkout Source Code:** Securely checks out the `main` branch of the `kaiburr-task1-java-api` repository.
2.  **Set up JDK 17:** Prepares the runner environment with the correct Java version.
3.  **Build with Maven:** Compiles the source code and creates the executable `.jar` file.
4.  **Login to Docker Hub:** Authenticates with Docker Hub using encrypted secrets stored in the repository settings.
5.  **Build and Push Docker Image:** Builds the Docker image and pushes it to the public registry, ready for deployment.

---

## ✅ Proof of Successful Execution

### 1. Successful Workflow Run
*The screenshot below shows a successful execution of the pipeline in the GitHub Actions tab.*

**[Drag and drop your screenshot of the green checkmark in the Actions list here]**

### 2. Published Docker Image
*This screenshot from Docker Hub confirms that the pipeline successfully built and pushed the `kaiburr-task-api:latest` image to the public registry.*

**[Drag and drop your screenshot of the Docker Hub repository page here]**
