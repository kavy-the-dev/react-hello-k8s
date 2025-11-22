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
2. Build the Docker image inside Minikube
bash
Copy code
eval $(minikube docker-env)
docker build -t kavybhavsar/react-hello:latest .
3. Apply the Kubernetes Deployment
bash
Copy code
kubectl apply -f deployment.yaml
4. Apply the Kubernetes Service
bash
Copy code
kubectl apply -f service.yaml
5. Verify Resources
bash
Copy code
kubectl get pods
kubectl get services
6. Open the Application in the Browser
bash
Copy code
minikube service react-hello-service
Minikube will automatically open the service URL in your browser.
