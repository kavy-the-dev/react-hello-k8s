React Hello Kubernetes Deployment

This project contains a React application deployed on Kubernetes using Minikube and Docker.

Prerequisites

Make sure you have:

Docker installed

kubectl installed

Minikube installed

How to Run
1. Start Minikube
minikube start

2. Build the Docker image inside Minikube
eval $(minikube docker-env)
docker build -t kavybhavsar/react-hello:latest .

3. Apply the Kubernetes Deployment
kubectl apply -f deployment.yaml

4. Apply the Kubernetes Service
kubectl apply -f service.yaml

5. Verify resources
kubectl get pods
kubectl get services

6. Open the application in the browser
minikube service react-hello-service


Minikube will automatically open the service URL in your browser.
