# Task-5_Internship

# NGINX Deployment and Service on Minikube Kubernetes

## Overview

This project demonstrates how to deploy a simple NGINX application on a Minikube Kubernetes cluster. It covers:

- Creating a Deployment for NGINX pods
- Exposing the deployment using a NodePort Service
- Scaling the deployment replicas
- Accessing the application locally via Minikube

---

## 1. Deployment

The **Deployment** manages the desired state of NGINX pods, ensuring the specified number of replicas are running.

### Explanation

- Defines the container image (`nginx:1.14.2`)
- Sets the number of replicas
- Defines container ports exposed internally by pods
- Labels the pods for Service selectors

### Starting minikube and applying deploymnet
![2](https://github.com/user-attachments/assets/57b242ee-e49e-40a2-8933-c12acaad6b30)
![3](https://github.com/user-attachments/assets/a84af155-fa4d-47ec-9291-4c3ec81ee35a)
![5](https://github.com/user-attachments/assets/402d7aa0-287b-4d86-ba45-080e0cdcc03e)


### 2. Service
The Service exposes the NGINX deployment to external clients by creating a NodePort that maps a port on the Minikube host to the pods.

### Explanation
  - Type is NodePort to allow access outside the cluster
  - Selects pods using the label app: nginx
  - Maps port 80 inside pods to a high port on Minikube (e.g., 30007)
![4](https://github.com/user-attachments/assets/000b575b-6aee-4546-94e2-53afbf3268c3)


---
### 3. Scaling the Deployment
![7](https://github.com/user-attachments/assets/b6645f18-dd1e-4970-b6c6-6dab56397b22)

---
### 4. Describe the pods
![6](https://github.com/user-attachments/assets/c972938a-06f0-41c6-b5b0-9791bef3751a)

---
### 5. Accessing the Application
![1](https://github.com/user-attachments/assets/e5d10bac-c8ed-43f1-baaf-fb6caa07f3ce)


