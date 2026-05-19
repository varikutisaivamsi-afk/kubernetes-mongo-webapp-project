# Kubernetes MongoDB WebApp Deployment

## Project Overview

This project demonstrates deploying a containerized web application with MongoDB on Kubernetes using Minikube.

The application was deployed locally using Docker-based Minikube on Windows and managed using Kubernetes YAML manifests.

---

## Technologies Used

* Kubernetes
* Minikube
* Docker
* MongoDB
* YAML
* kubectl

---

## Kubernetes Components Used

* Deployment
* Service
* ConfigMap
* Secret
* Pods
* NodePort

---

## Project Architecture

WebApp Pod ---> Mongo Service ---> MongoDB Pod

---

## Files Included

| File Name         | Description                            |
| ----------------- | -------------------------------------- |
| mongo.yaml        | MongoDB Deployment and Service         |
| mongo-config.yaml | MongoDB ConfigMap                      |
| mongo-secret.yaml | MongoDB Secret                         |
| webapp.yaml       | Web Application Deployment and Service |

---

## Features Implemented

* MongoDB Deployment
* Web Application Deployment
* ConfigMap Configuration
* Kubernetes Secrets
* NodePort Service Exposure
* Pod Scaling
* Self-Healing Pods
* Kubernetes Troubleshooting

---

## Steps to Run the Project

### 1. Start Minikube

```bash
minikube start --driver=docker
```

### 2. Apply ConfigMap

```bash
kubectl apply -f mongo-config.yaml
```

### 3. Apply Secret

```bash
kubectl apply -f mongo-secret.yaml
```

### 4. Deploy MongoDB

```bash
kubectl apply -f mongo.yaml
```

### 5. Deploy Web Application

```bash
kubectl apply -f webapp.yaml
```

### 6. Verify Resources

```bash
kubectl get all
```

### 7. Open Application

```bash
minikube service webapp-service
```

---

## Useful Kubernetes Commands

### Check Pods

```bash
kubectl get pods
```

### Check Services

```bash
kubectl get svc
```

### View Logs

```bash
kubectl logs <pod-name>
```

### Describe Pod

```bash
kubectl describe pod <pod-name>
```

### Scale Deployment

```bash
kubectl scale deployment webapp-deployment --replicas=3
```

---

## Learning Outcomes

Through this project, I learned:

* Kubernetes architecture basics
* YAML configuration management
* Deployments and Services
* ConfigMaps and Secrets
* Pod networking
* Container orchestration
* Kubernetes troubleshooting
* Minikube cluster management

---

## Future Improvements

* Deploy on Azure AKS / AWS EKS
* Add Helm Charts
* Implement CI/CD pipeline
* Add Ingress Controller
* Configure Persistent Volumes
* Add Monitoring with Prometheus and Grafana

---

## Author

Venkata Sai Vamsi
