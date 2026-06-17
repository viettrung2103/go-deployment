# Bookmark System Deployment

Repository này chứa toàn bộ cấu hình hạ tầng, môi trường và script để triển khai (deploy) hệ thống Bookmark Management sử dụng Docker Compose và Nginx Reverse Proxy.

This repository contains the complete configuration, environment, and scripts to deploy the Bookmark Management system using Docker Compose and Nginx Reverse Proxy.

## 🏛️ System Architecture Diagram

The app is designed following the Microservices/Multi-container. Connection is done via Docker with Network Bridge, public port is :80 (HTTP)


<img width="1100" height="491" alt="Screenshot 2026-06-12 at 17 04 15" src="https://github.com/user-attachments/assets/dd261012-67d5-4dc9-8c34-42d3a69a213b" />
<img width="852" height="693" alt="Screenshot 2026-06-12 at 16 57 27" src="https://github.com/user-attachments/assets/4b448521-7f4e-4cb2-975f-3734d0e130fe" />

## 🚀 Deployment Guide

### Prerequisites
- [Docker](https://docs.docker.com/get-docker/) installed.
- [Docker Compose](https://docs.docker.com/compose/install/) plugin installed.

### Execution Steps
1. Clone this deployment configuration repository to your machine or server:
```bash
   git clone [https://github.com/viettrung21/bookmark-deployment.git](https://github.com/viettrung21/bookmark-deployment.git)
   cd bookmark-deployment
```
2. Initialize your runtime environment file:
```bash
    cp .env.example.example .env.example
   # Edit the .env.example file values to suit your environment needs
```
3. Spin up the entire infrastructure stack in detached mode:
```bash
docker compose up -d
```
4. Verify that all targeted services are up and active:
```bash
   docker compose ps
```
The application is now accessible via reverse proxy at http://localhost.