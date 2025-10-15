# Kubernetes Demo Application with Express.js and Nginx

This is a demonstration application designed to showcase Kubernetes Ingress functionality. The application is built with Express.js and includes features to demonstrate various aspects of Kubernetes networking and service discovery.

## Features

- **Interactive Web Interface**: UI displaying:
  - Pod name and Node IP information
  - Application uptime tracking
  - Random Kubernetes fun facts
  - Current time display
  
- **Multiple Endpoints**:
  - `/` - Main application interface
  - `/nginx` - Internal service communication demo (ClusterIP)
  - `/external-api` - External API integration example
  - `/healthz` - Health check endpoint for Kubernetes probes

## Docker Image

The application is available as a Docker image on Docker Hub:
[dmitryzhuravlev/k8s-web-express-nginx](https://hub.docker.com/r/dmitryzhuravlev/k8s-web-express-nginx)

To pull the image:
```bash
docker pull dmitryzhuravlev/k8s-web-express-nginx
```

## Technical Details

- Built with Express.js 5.1.0
- Base image: Node.js Alpine
- Exposes port 3000
- Includes health check endpoint
- Demonstrates inter-service communication with Nginx

## Kubernetes Integration

This application is specifically designed for demonstrating Kubernetes Ingress setup. It includes features that make it ideal for learning and testing Kubernetes networking concepts:

- Service discovery demonstration
- Load balancing readiness
- Health check implementation
- Inter-service communication examples

[Kubernetes Ingress Setup Guide](link-to-be-added-later)

## Running Locally

1. Clone the repository
2. Install dependencies:
   ```bash
   npm install
   ```
3. Start the application:
   ```bash
   npm start
   ```
   The application will be available at http://localhost:3000

## Container Environment Variables

The application uses the following environment variables:
- `HOSTNAME` - Pod name (automatically set by Kubernetes)
- Port 3000 is exposed for HTTP traffic

