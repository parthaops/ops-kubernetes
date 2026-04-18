
# 🚀 PARTHAOPS

**Ops-Kubernetes** is a hands-on **Kubernetes workspace repository** created to practice, manage, and experiment with **real‑world Kubernetes YAML manifests**.  
It acts as a centralized lab for learning Kubernetes concepts and implementing **production‑oriented DevOps & SRE patterns**.

***

## 📌 Purpose of This Repository

*   Serve as a **workspace for Kubernetes (K8s) YAML manifests**
*   Maintain **reusable, modular configurations**
*   Practice **real‑world DevOps & SRE workflows**
*   Build a strong **Kubernetes / DevOps portfolio**

***

## 📂 Repository Scope

This repository includes commonly used Kubernetes components:

### 🔹 Namespaces

### 🔹 Workloads

*   Deployments
*   StatefulSets
*   DaemonSets
*   Jobs & CronJobs

### 🔹 Services

*   ClusterIP
*   NodePort
*   LoadBalancer

### 🔹 Configuration

*   ConfigMaps
*   Secrets

### 🔹 Networking

*   Ingress
*   Network Policies

### 🔹 Storage

*   PersistentVolumes (PV)
*   PersistentVolumeClaims (PVC)
*   StorageClasses

### 🔹 Operations

*   Health checks
*   Resource requests & limits
*   Autoscaling basics

***

## 🛠️ What You’ll Find Here

*   Namespace examples
*   Deployment & DaemonSet manifests
*   Stateful applications with persistent storage
*   Service & Ingress routing
*   Configuration management using ConfigMaps & Secrets
*   Autoscaling and operational best practices

✅ All manifests are:

*   Simple & readable
*   Modular & reusable
*   Written close to **production standards**

***

## ⚙️ kubectl Command Cheat Sheet

### 🔹 Cluster & Context

```bash
kubectl version
kubectl cluster-info
kubectl api-resources
kubectl config get-contexts
kubectl config current-context
kubectl config use-context <context>
```

### 🔹 Namespace Management

```bash
kubectl get ns
kubectl create ns <namespace>
kubectl delete ns <namespace>
kubectl describe ns <namespace>
kubectl config set-context --current --namespace=<namespace>
```

### 🔹 Apply & Delete Manifests

```bash
kubectl apply -f file.yaml
kubectl apply -f directory/
kubectl delete -f file.yaml
kubectl delete -f directory/
kubectl diff -f file.yaml
```

### 🔹 Pods (Debugging)

```bash
kubectl get pods
kubectl get pods -A
kubectl describe pod <pod-name>
kubectl logs <pod-name>
kubectl logs <pod-name> -c <container-name>
kubectl exec -it <pod-name> -- /bin/sh
kubectl delete pod <pod-name>
```

### 🔹 Workloads

```bash
kubectl get deploy
kubectl get ds
kubectl get sts
kubectl get jobs
kubectl describe deploy <name>
kubectl rollout status deploy/<name>
kubectl rollout restart deploy/<name>
kubectl scale deploy <name> --replicas=3
```

### 🔹 Services & Networking

```bash
kubectl get svc
kubectl describe svc <service-name>
kubectl get ingress
kubectl describe ingress <ingress-name>
kubectl get networkpolicy
```

### 🔹 ConfigMaps & Secrets

```bash
kubectl get cm
kubectl get secret
kubectl describe cm <name>
kubectl describe secret <name>
kubectl create configmap app-config --from-literal=key=value
kubectl create secret generic app-secret --from-literal=password=secret
```

### 🔹 Storage

```bash
kubectl get pv
kubectl get pvc
kubectl describe pvc <name>
kubectl get storageclass
```

### 🔹 Autoscaling

```bash
kubectl get hpa
kubectl describe hpa <name>
kubectl autoscale deploy <name> --min=1 --max=5 --cpu-percent=70
```

### 🔹 Monitoring & Troubleshooting

```bash
kubectl top nodes
kubectl top pods
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl explain <resource>
```

***

## 🚀 How to Use

```bash
git clone https://github.com/parthaops/ops-kubernetes.git
cd ops-kubernetes
kubectl apply -f .
```

> ⚠️ **Note:**  
> This repository is intended for **learning and lab environments**.  
> Always review manifests before using them in production.

***

## 👨‍💻 Author

**Partha**  
Cloud | DevOps | Kubernetes  
Signature: **parthaops**

***

## 📜 License & Copyright

© 2026 **parthaops**  
All rights reserved.
