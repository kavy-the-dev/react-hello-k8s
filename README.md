# React Hello Kubernetes Deployment

This project contains a React application deployed on Kubernetes using Minikube and Docker.

## Prerequisites

Make sure you have the following installed:

- Docker
- kubectl
- Minikube

## How to Run

### 1. Start Minikube
```bash
minikube start
```
2. Build the Docker image inside Minikube

This ensures the image is available inside the Minikube cluster.
```bash
eval $(minikube docker-env)
docker build -t kavybhavsar/react-hello:latest .
```
3. Apply the Kubernetes Deployment
```bash
kubectl apply -f deployment.yaml
```
4. Apply the Kubernetes Service
```bash
kubectl apply -f service.yaml
```
5. Verify that everything is running
```bash
kubectl get pods
kubectl get services
```

You should see:

A pod named react-hello

A service named react-hello-service

6. Open the Application in the Browser
```bash
minikube service react-hello-service
```

Minikube will automatically open the service URL in your browser.
