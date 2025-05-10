# 🐳 MongoDB + Mongo-Express on Kubernetes

This is a simple Kubernetes deployment of **MongoDB** and **Mongo-Express**, demonstrating how to manage configuration, services, and secrets in a real-world cluster setup.

---

## 🚀 Project Structure

This project includes:

- `mongodb-deployment.yaml`: Contains both the Deployment and Service for MongoDB, combined in one file for easier setup
- `mongo-express.yaml`: Contains the Deployment for Mongo-Express (web UI) and the NodePort Service to access it from outside the Kubernetes cluster
- `mongo-configmap.yaml`: ConfigMap to store MongoDB URL
- `mongo-secret.yaml`: Secret to store the MongoDB username and password

---

## 📦 Requirements

- A running Kubernetes cluster (e.g., Minikube or Kind)
- `kubectl` installed and configured

---

## 🛠️ How to Deploy

1. Clone the repository:

```bash
git clone https://github.com/Roslaan001/my-first-k8s-project-mongodb-and-express
```

---

2. Apply the Kubernetes manifests:


kubectl apply -f mongo-secret.yml
kubectl apply -f mongo-configmap.yml
kubectl apply -f mongodb-deployment.yml
kubectl apply -f mongo-service.yaml
kubectl apply -f mongo-express.yml

---

3. Access Mongo-Express:

If using Minikube:

minikube service mongo-express-service

---

📚 What I Learned
- Using ConfigMaps to inject configuration

- Using Secrets to handle sensitive data

- Managing multiple deployments and services

- Exposing services internally (ClusterIP) and externally (NodePort)


