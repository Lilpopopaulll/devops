# Docker Lab Report

## Main Purpose of the Lab

The main goal of this lab was to understand and practice the core concepts of **Docker** and **containerization**.  
Through this lab, I learned how to:
- Install and verify Docker installation.
- Write a `Dockerfile` and build Docker images.
- Run and manage Docker containers using various options.
- Push and share Docker images on **Docker Hub**.
- Use **Docker Compose** to run multiple containers that interact with each other (Node.js + Redis).

---

## Possible Application in a Company

Docker is widely used in companies to:
- Ensure that software runs identically across all environments (development, staging, production).
- Simplify **deployment**.
- Improve **scalability**.
- Facilitate **continuous integration and continuous deployment (CI/CD)**.

Example:  
In a company developing a web platform, Docker can be used to create a consistent environment for developers, test features in isolation, and deploy updates to production with minimal risk.

---

## Step in the DevOps Cycle

This lab corresponds mainly to the **"Build"** and **"Deploy"** phases of the **DevOps cycle**, which typically follows this flow:

Plan → Code → Build → Test → Release → Deploy → Operate → Monitor → (feedback loop)


### Justification:
- **Build**: I built Docker images from the application source code using a `Dockerfile`.
- **Deploy**: I deployed and ran containers locally, and used Docker Compose to manage multi-container setups.
- It also partially touches **Operate**, since I used `docker logs`, `docker ps`, and `docker stop` to monitor and control containers.

---

## Problems Encountered and Solutions

### 1. Port Already in Use
**Problem:** When running `docker run -p 12345:8080`, I got an error because the port 12345 was already in use.  
**Solution:** I stopped the previous container using `docker stop <CONTAINER_ID>` and re-ran the command with a different port.  
**Resources:**  
- [Docker run reference](https://docs.docker.com/engine/reference/run/)

---

### 2. Docker Compose Configuration Error
**Problem:** My first `docker-compose.yaml` file was incomplete, causing an error:  services.web.build contains an invalid type, it should be a string

**Solution:** I fixed the indentation and correctly defined the `build` context.  
**Resources:**  
- [Compose file reference](https://docs.docker.com/compose/compose-file/)

---

## Final State of the Lab

At the end of the lab:
- The Node.js app was successfully containerized and could run on any system.
- The Redis service worked correctly with Docker Compose.
- I was able to share my image on Docker Hub and pull it from another account.
- The counter persistence worked correctly using Docker Volumes.