# 🐳 Jenkins Docker Image
A ready-to-use Jenkins Docker image with Docker support, pre-installed plugins, and automatic initial configuration.

![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Jenkins](https://img.shields.io/badge/Jenkins-D24939?style=for-the-badge&logo=jenkins&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)
![Debian](https://img.shields.io/badge/Debian-12-A81D33?style=for-the-badge&logo=debian&logoColor=white)

## Features
- Jenkins LTS
- Docker CLI installed
- Docker socket support
- Pre-installed Jenkins plugins
- Automatic admin user creation
- Configuration as Code (JCasC)
- Ready for CI/CD pipelines
## Project Structure
```text
.
├── Dockerfile
├── docker-compose.yml
├── plugins.txt
├── casc/
├── jenkins.yaml
└── README.md
```
## Requirements
- Docker
- Docker Compose
## Quick Start
Clone the repository:
```bash
git clone https://github.com/gutamurr/jenkins-docker-image.git
cd jenkins-docker-image
```
Build and start Jenkins:
```bash
docker compose up --build -d
```
Open Jenkins in your browser:
```text
http://localhost:8000
```
## Default Credentials
| Username | Password |
|----------|----------|
| admin | admin |
> **Note:** Change the default credentials before using this project outside of a local environment.
## Docker Support
The container uses the host Docker daemon through:
```text
/var/run/docker.sock
```
This allows Jenkins pipelines to build and run Docker containers without Docker-in-Docker.
## Customization
You can customize:
- Installed plugins (`plugins.txt`)
- Jenkins Configuration as Code (`jenkins.yaml`)
## License
This project is licensed under the MIT License.
