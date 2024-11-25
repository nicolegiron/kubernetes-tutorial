Kubernetes Cluster Setup

This repository documents my setup of a Kubernetes (K8s) cluster following a tutorial. It includes key configuration files and steps to deploy applications.

---

Overview

- Set up a Kubernetes cluster using Minikube.
- Deployed MongoDB and Mongo Express applications.
- Managed Kubernetes objects like Deployments, Services, ConfigMaps, and Secrets.

---

Tools Used

- Kubernetes
- Minikube
- kubectl
- Docker

---

Files in This Repo

- mongo-deployment.yaml: Deployment for MongoDB.
- mongo-express-deployment.yaml: Deployment for Mongo Express.
- service.yaml: Service definitions.
- configmap.yaml: Configuration settings.
- secret.yaml: Secure credentials.

---

How to Set It Up

1. Start Minikube:
   minikube start

2. Apply Configurations:
   kubectl apply -f mongo-deployment.yaml
   kubectl apply -f mongo-express-deployment.yaml
   kubectl apply -f service.yaml
   kubectl apply -f configmap.yaml
   kubectl apply -f secret.yaml

3. Access Mongo Express:
   - Use Minikube:
     minikube service mongo-express-service
   - Or Port Forward:
     kubectl port-forward service/mongo-express-service 8081:8081

   Open your browser and go to http://localhost:8081.

---

Learnings

- Set up a Kubernetes cluster with Minikube.
- Deployed apps using Kubernetes objects like Deployments and Services.
- Used ConfigMaps and Secrets to manage configurations and credentials.

---

Author

- Nicole Giron
  GitHub: [nicolegiron](https://github.com/nicolegiron)
