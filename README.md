# Dockerized App

## Project Overview

**dockerized-app** is a simple web application frontend that demonstrates a complete CI/CD pipeline using Jenkins, SonarQube, and Docker. The application is designed to facilitate continuous integration and deployment while maintaining code quality.

## Features

- Simple frontend application built with HTML/CSS.
- Continuous Integration with Jenkins running in a Docker container.
- Automated code quality checks using SonarQube.
- Deployment of the application via Docker, accessible to users.

## Getting Started

### Prerequisites

- Docker installed on your machine.
- Jenkins running in a Docker container.
- SonarQube set up and running.

### Setup

1. Clone the repository:
   ```bash
   git clone https://github.com/iqbalalisha/Dockerized-app.git
   cd dockerized-app
   ```

2. Build the Docker image:
   ```bash
   docker build -t my-frontend-app .
   ```

3. Run the Docker container:
   ```bash
   docker run -d -p 85:80 my-frontend-app
   ```

4. Access the application at `http://localhost:85`.

### CI/CD Pipeline

- **Jenkins**: Configure Jenkins with a pipeline that pulls the latest code from GitHub, runs builds, and performs SonarQube analysis.
- **Webhooks**: GitHub webhooks are set up to trigger Jenkins jobs on code commits.
- **SonarQube Integration**: Continuous code quality checks are performed through SonarQube during the build process.


## Acknowledgments

- [Jenkins](https://www.jenkins.io/)
- [SonarQube](https://www.sonarqube.org/)
- [Docker](https://www.docker.com/)
```

