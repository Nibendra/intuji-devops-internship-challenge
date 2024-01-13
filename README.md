# Intuji DevOps Internship Challenge

## Overview

This project documents the steps undertaken during the Intuji DevOps Internship Challenge. The goal is to set up a CI/CD pipeline using Docker, Jenkins, and GitHub.

## Prerequisites

- Ubuntu 22.04 LTS
- Git
- Docker
- Jenkins

## Steps

1. Installing Docker
- Execute the "install_docker.sh" script to install Docker on Ubuntu. Verify the installation using the "docker run hello-world" command.

2. Cloning GitHub repository:
- Cloned the github repository using "git clone https://github.com/silarhi/php-hello-world.git" command.
- Two Dockerfiles were created for nginx and apache web servers : Dockerfile.nginx and Dockerfile.apache, with their necessary configurations.
- Docker images were built using "docker build" command.
- The docker images were then pushed to docker hub using "docker push" command. Login credentials to docker hub were used to push the images.

3. Creating Docker compose files:
- Docker compose files - "docker_compose.nginx.yml" and "docker_compose.apache.yml" - were created with the necessary configurations.
- The containers were started using "docker compose up" command. Running containers were checked using "docker ps" command.

4. Installing jenkins
- Jenkins was installed using the apt repository. Execute the "install_jenkins.sh" bash script.
- After installation, jenkins was setup and necessary plugins were installed.
- Then, Docker was configured in jenkins using the cloud option.
- After that, a freestyle project was created on jenkins dashboard. It was configured with git repository and an execute shell command was added, which built the Docker images and pushed them to DockerHub.
- The jenkins job was run manually by clicking on "Build Now".

5. Uploading to GitHub
- The code and scripts were added to github throughout the process. Screenshots of each step are also available in the "Screenshots" folder.
