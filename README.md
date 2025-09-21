# **Kubernetes Learning Repository**

Welcome to this Kubernetes repository! 🚀  
This repo is a collection of Kubernetes configuration files, manifests, and practice examples designed to deepen understanding of how Kubernetes works in real-world scenarios.  

---

## **📖 Overview**

The repository includes examples for:

- **Pod** – the most basic workload unit in Kubernetes  
- **Deployment** – declarative management of Pods (scaling, updates)  
- **ReplicaSet** – maintaining desired Pod replicas  
- **Service** – exposing and connecting workloads  
- **Ingress** – external access to the Django app (via HTTP routes)  
- **PersistentVolume & PersistentVolumeClaim** – data storage for the app  
- **Job** – run a one-off task (useful for batch jobs or migrations)  
- **CronJob** – run scheduled tasks in the cluster (like nightly DB cleanups)  
- **DaemonSet** – run agents or pods on every node in the cluster  

Basically, this repo showcases almost all the “Greatest Hits” of Kubernetes resources. 🎶  

---

## **🚦 Prerequisites**

Make sure you have:  

- A running Kubernetes cluster (Minikube, Kind, or cloud provider)  
- `kubectl` installed and pointing to your cluster  
- Docker installed if you want to build your own app images  

---

## **🛠️ Usage**

### **1. Clone the repository**

**Bash**
```bash
git clone https://github.com/Himanshu31bisht/kubernetes.git
cd kubernetes
2. Apply resources individually
Bash

Bash

kubectl apply -f pod.yaml
kubectl apply -f deployment.yaml
kubectl apply -f service.yaml
kubectl apply -f ingress.yaml
kubectl apply -f pv.yaml
kubectl apply -f pvc.yaml
kubectl apply -f job.yaml
kubectl apply -f cronjob.yaml
kubectl apply -f deamonset.yaml
kubectl apply -f ReplicaSet.yaml
3. Apply everything at once
If you’re feeling bold (or just efficient 😉):

Bash

Bash

kubectl apply -f .
This will create all resources in one go: Pods, Deployments, Services, Ingress, PV, PVC, Jobs, CronJobs, DaemonSets, and ReplicaSets.

4. Verify deployments
Bash

Bash

kubectl get pods
kubectl get deployments
kubectl get svc
kubectl get ingress
kubectl get pv,pvc
kubectl get jobs,cronjobs
kubectl get rs
kubectl get ds
5. Cleanup
When you’re done experimenting (and want to give your cluster a break):

Bash

Bash

kubectl delete -f .
⚙️ Repository Structure
text

kubernetes/
├── django-notes-app/        # Django application project
├── pod.yaml                 # Basic pod manifest
├── deployment.yaml          # Deployment for django app
├── ReplicaSet.yaml          # ReplicaSet example
├── service.yaml             # ClusterIP/LoadBalancer service
├── ingress.yaml             # Ingress rules for app routing
├── pv.yaml                  # Persistent Volume
├── pvc.yaml                 # Persistent Volume Claim
├── job.yaml                 # One-off job
├── cronjob.yaml             # Recurring schedule job
├── deamonset.yaml           # DaemonSet resource
└── README.md
🎯 Goal
The goal of this repo is to provide a one-stop Kubernetes learning environment with a real Django app at its core. By experimenting with these manifests, you’ll not only deploy a working web service but also grasp the roles of various Kubernetes resources.

🙌 Contributions
Kubernetes is a vast ocean 🌊. If you have improvements, better manifests, or new examples—contributions are very welcome. Fork and PR away!
