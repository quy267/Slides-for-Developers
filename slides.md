---
theme: default 
background: https://source.unsplash.com/collection/94734566/1920x1080
class: 'text-center'
---

# Docker Jenkins CI/CD Pipeline

## Introduction

---

# Agenda

<style>
h1 {
  text-align: center;
}
</style>

- Why Docker
- Jenkins Pipeline
- Scenarios Implementation
- Demo

---

# Why Docker ?

<style>
h1 {
  text-align: center;
}
</style>

- Isolation
- Lightweight
- Simplicity
- Workflow
- Community

---

# Docker Engine

<style>
h1 {
  text-align: center;
}
</style>

- Docker Daemon
- Docker CLI

---

# Docker Daemon

<style>
h1 {
  text-align: center;
}
</style>

- Builds Images
- Runs and Manages Containers
- RESTFUL API

---

# Docker CLI

<style>
h1 {
  text-align: center;
}
</style>

- docker build # Build an image from a Dockerfile
- docker images # List all images on a Docker host
- docker run # Run an image
- docker ps # List all running and stopped instances
- docker stop # Stop a running instances
- docker rm # Remove an instance
- docker rmi # Remove an image

---

# Docker Architecture

<style>
h1 {
  text-align: center;
}
</style>

<img src="/Docker_Architecture.png" class="rounded" style="height:60vh"/>

---

# Docker Hub

<style>
h1 {
  text-align: center;
}
</style>

- Provides Docker Services
- Library of public images
- Storage for your images
- Free for public images
- Cost for private images

---

# Jenkins Pipeline

<style>
h1 {
  text-align: center;
}
</style>

- Pipeline as Code
    * Capture the entire continuous delivery process
    * Check a Jenkinsfile into your source repo
- jenkins.io/doc/book/pipeline

---

# Scenarios Implementation

<style>
h1 {
  text-align: center;
}
</style>

<img src="/1_MyncGrSowUxZCwehBVKHtg.jpeg" class="rounded" style="height:60vh"/>

---

# Planning the pipeline

<style>
h1 {
  text-align: center;
}
</style>

- Stages desired:
    - Build
    - Test
        - Unit
        - Performance
        - Front-end
    - Static Analysis
    - Deployment

---

# Build

<style>
h1 {
  text-align: center;
}
</style>

- Goal:
    - Perform a reproducible build – Create an artifact which can used later
        - To run tests against
        - To deploy to an environment
    - In this case, we're using Docker.

---

# Deployment

<style>
h1 {
  text-align: center;
}
</style>

- "Deployment" may have different meanings
    - Deploying to AWS/Azure 
    - Deploying to a physical datacenter 
    - Uploading to an app store 
    - Uploading to an internal artifact server

---

# Demo 


<style>
h1 {
  text-align: center;
}
</style>

<img src="/aws_ecs.png" class="rounded" style="height:60vh"/>