# Continuous Integration Pipeline using GitHub Actions

## Overview

This project demonstrates a simple Continuous Integration (CI) pipeline using GitHub Actions.

Whenever code is pushed to the main branch, GitHub Actions automatically triggers a workflow that builds and validates a Dockerized Java application. This helps identify build issues early and reduces manual effort.

## Tech Stack

* Java 17
* Docker
* GitHub Actions
* Git
* GitHub
* Ubuntu (WSL)

## Project Structure

```text
ci-cd-github-actions/
├── src/
│   └── Main.java
├── Dockerfile
├── .github/
│   └── workflows/
│       └── docker-ci.yml
└── README.md
```

## Workflow

```text
Code Change
      ↓
Git Push
      ↓
GitHub Actions Trigger
      ↓
Checkout Repository
      ↓
Build Docker Image
      ↓
Run Docker Container
      ↓
Success / Failure
```

## Docker Build

The workflow automatically builds a Docker image using the Dockerfile whenever code is pushed to the repository.

```bash
docker build -t ci-cd-java-app .
```

## Docker Run

After building the image, the workflow runs the container to validate that the application executes successfully.

```bash
docker run ci-cd-java-app
```

## Workflow Configuration

The GitHub Actions workflow file is located at:

```text
.github/workflows/docker-ci.yml
```

The workflow performs the following actions:

1. Checks out the repository.
2. Builds the Docker image.
3. Runs the Docker container.
4. Reports the build status.

## Screenshots

### Workflow Overview

<img width="1491" height="396" alt="Screenshot 2026-06-05 184235" src="https://github.com/user-attachments/assets/04addb19-dca5-4dbe-bd3e-54ff4c6bce2d" />

### Workflow Success

<img width="1422" height="457" alt="Screenshot 2026-06-05 184247" src="https://github.com/user-attachments/assets/7e51b233-12a4-4a84-8de0-1b0326bfbdc6" />

## Key Learnings

* GitHub Actions workflow creation
* Continuous Integration concepts
* Docker image automation
* Automated build validation
* Git and GitHub workflow management

## Conclusion

This project successfully implements a Continuous Integration pipeline using GitHub Actions. The workflow automatically validates application changes by building and running a Dockerized Java application whenever code is pushed to the repository.

## Author

Suriya M
