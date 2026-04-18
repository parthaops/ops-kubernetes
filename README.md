Perfect 👍  
Below is an **enhanced, professional, and DevOps‑grade README.md**, written **as a README file writer**, keeping your original content intact and **adding a complete, popular `kubectl` command section** that is:

*   ✅ Practical (used daily by DevOps/SREs)
*   ✅ Well‑organized
*   ✅ Easy to skim
*   ✅ Portfolio & interview ready

You can **copy‑paste this directly**.

***

````markdown
# PARTHAOPS

PARTHAOPS is a hands-on **Kubernetes workspace repository** designed to store, manage, and experiment with real‑world **Kubernetes YAML manifests**.  
This repository acts as a centralized lab for building, testing, and maintaining Kubernetes components from scratch using best practices.

---

## 📌 Purpose of This Repository
- Act as a **workspace for Kubernetes (K8s) YAML files**
- Maintain reusable and modular configurations
- Practice production‑ready infrastructure patterns
- Serve as a reference for real‑world DevOps and SRE use cases

---

## 📂 Repository Structure
The repository covers most commonly used Kubernetes resources, including:

- **Namespaces**
- **Workloads**
  - Deployments
  - StatefulSets
  - DaemonSets
  - Jobs & CronJobs
- **Services**
  - ClusterIP
  - NodePort
  - LoadBalancer
- **Config & Secrets**
  - ConfigMaps
  - Secrets
- **Networking**
  - Ingress
  - Network Policies
- **Storage**
  - PersistentVolumes (PV)
  - PersistentVolumeClaims (PVC)
  - StorageClasses
- **Observability & Ops**
  - Health probes
  - Resource requests & limits
  - Pod disruption basics

---

## 🛠️ Examples Included
This repository provides **example YAML manifests** such as:

- Namespace creation
- Sample Deployment with replicas
- DaemonSet for node‑level agents
- Stateful workloads with persistent storage
- Service and Ingress mapping
- Environment‑based configurations using ConfigMaps and Secrets

All examples are written to be:
- Easy to read
- Modular
- Reusable
- Close to production standards

---

## ⚙️ Popular & Essential kubectl Commands (Complete Cheat Sheet)

### 🔹 Cluster & Context Management
```bash
kubectl version
kubectl cluster-info
kubectl api-resources
kubectl api-versions

kubectl config get-contexts
kubectl config current-context
kubectl config use-context <context>
````

***

### 🔹 Namespace Operations

```bash
kubectl get ns
kubectl create ns <namespace>
kubectl delete ns <namespace>
kubectl describe ns <namespace>

kubectl config set-context --current --namespace=<namespace>
```

***

### 🔹 Apply, Update & Delete Manifests

```bash
kubectl apply -f file.yaml
kubectl apply -f directory/
kubectl delete -f file.yaml
kubectl delete -f directory/
kubectl diff -f file.yaml
```

***

### 🔹 Resource Inspection

```bash
kubectl get all
kubectl get all -n <namespace>
kubectl describe <resource> <name>
```

***

### 🔹 Pods (Debugging & Troubleshooting)

```bash
kubectl get pods
kubectl get pods -A
kubectl describe pod <pod-name>

kubectl logs <pod-name>
kubectl logs <pod-name> -c <container-name>

kubectl exec -it <pod-name> -- /bin/sh
kubectl delete pod <pod-name>
```

***

### 🔹 Workloads (Deployments, DaemonSets, Jobs)

```bash
kubectl get deploy
kubectl get ds
kubectl get jobs
kubectl describe deploy <deployment-name>

kubectl rollout status deploy/<deployment-name>
kubectl rollout history deploy/<deployment-name>
kubectl rollout restart deploy/<deployment-name>

kubectl scale deploy <deployment-name> --replicas=3
```

***

### 🔹 Services

```bash
kubectl get svc
kubectl describe svc <service-name>

kubectl expose deploy <deployment-name> \
  --type=NodePort \
  --port=80
```

***

### 🔹 Ingress & Networking

```bash
kubectl get ingress
kubectl get ingress -A
kubectl describe ingress <ingress-name>

kubectl get networkpolicy
```

***

### 🔹 ConfigMaps & Secrets

```bash
kubectl get cm
kubectl get secret

kubectl describe cm <configmap-name>
kubectl describe secret <secret-name>

kubectl create configmap app-config \
  --from-literal=key=value

kubectl create secret generic app-secret \
  --from-literal=password=secret
```

***

### 🔹 StatefulSets

```bash
kubectl get sts
kubectl describe sts <statefulset-name>
kubectl rollout status sts/<statefulset-name>

kubectl delete pod <pod-name>   # Validate persistence
```

***

### 🔹 Storage

```bash
kubectl get pv
kubectl get pvc
kubectl describe pvc <pvc-name>
kubectl get storageclass
```

***

### 🔹 Autoscaling (HPA)

```bash
kubectl get hpa
kubectl describe hpa <hpa-name>

kubectl autoscale deploy <deployment-name> \
  --min=1 --max=5 --cpu-percent=70
```

***

### 🔹 Events, Metrics & Explain

```bash
kubectl get events --sort-by=.metadata.creationTimestamp
kubectl top nodes
kubectl top pods

kubectl explain <resource>
kubectl explain deploy.spec.template.spec
```

***

## 🚀 How to Use

```bash
git clone https://github.com/parthaops/ops-kubernetes.git
cd ops-kubernetes
kubectl apply -f .
```

> ⚠️ This repository is intended for **learning, practice, and lab environments**.  
> Always review and validate manifests before production use.

***

## 👨‍💻 Author

**Partha**  
Cloud | DevOps | Kubernetes  
Signature: **parthaops**

***

## 📜 Copyright

© 2026 **parthaops**  
All rights reserved.
