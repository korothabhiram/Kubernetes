# ☸️ Kubernetes

## 📘 What is Kubernetes?

Kubernetes (K8s) is an open-source **container orchestration platform** that automates the deployment, scaling, healing, and management of containerized applications. It groups containers into logical units (Pods) and schedules them across a cluster of machines, handling networking, storage, and failover so you don't have to do it by hand.

---

## 🙋‍♂️ Who Should Use Kubernetes?

- **DevOps Engineers**: Automate deployment and scaling of containerized workloads.
- **SREs**: Achieve self-healing, highly available infrastructure.
- **Cloud Architects**: Run consistent workloads across on-prem and multi-cloud.
- **Developers**: Ship and roll back releases without manual server juggling.
- **Tech Learners**: Understand how modern, cloud-native infrastructure actually runs.

---

## 🎯 Why Use Kubernetes?

- 🔄 Self-healing—restarts, reschedules, and replaces failed containers
- 📈 Automatic scaling based on load
- 🚀 Declarative, rolling deployments and easy rollbacks
- 🌐 Built-in service discovery and load balancing
- 🧩 Portable across cloud providers and on-prem

---
# ☸️ Top Kubernetes Commands Cheat Sheet

A handy, stylish list of the **most useful `kubectl` commands** you'll use for pods, deployments, services, and cluster management. Perfect for beginners and pros alike!

---

## 🧭 Cluster Info

| Command | Description |
|--------|-------------|
| `kubectl cluster-info` | 🌐 Show cluster endpoint info |
| `kubectl version` | 🔢 Show client/server version |
| `kubectl get nodes` | 🖥️ List cluster nodes |
| `kubectl describe node <node>` | 🔍 Detailed node info |
| `kubectl config get-contexts` | 📋 List available contexts |
| `kubectl config use-context <ctx>` | 🔀 Switch context |
| `kubectl config current-context` | 📍 Show active context |

---

## 📦 Pods

| Command | Description |
|--------|-------------|
| `kubectl get pods` | 👀 List pods in current namespace |
| `kubectl get pods -A` | 🌍 List pods across all namespaces |
| `kubectl get pods -o wide` | 📋 List pods with extra details (node, IP) |
| `kubectl describe pod <pod>` | 🔍 Detailed info about a pod |
| `kubectl logs <pod>` | 📜 View pod logs |
| `kubectl logs -f <pod>` | 📡 Follow real-time logs |
| `kubectl exec -it <pod> -- bash` | 💻 Access shell inside a pod |
| `kubectl delete pod <pod>` | 🧹 Delete a pod |
| `kubectl port-forward <pod> 8080:80` | 🔌 Forward local port to pod |

---

## 🚀 Deployments & ReplicaSets

| Command | Description |
|--------|-------------|
| `kubectl get deployments` | 📋 List deployments |
| `kubectl create deployment <name> --image=<image>` | 🆕 Create a deployment |
| `kubectl scale deployment <name> --replicas=3` | 📈 Scale a deployment |
| `kubectl rollout status deployment/<name>` | 📊 Check rollout status |
| `kubectl rollout history deployment/<name>` | 🕰️ Show rollout history |
| `kubectl rollout undo deployment/<name>` | ⏪ Roll back to previous revision |
| `kubectl set image deployment/<name> <container>=<image>` | 🔁 Update container image |
| `kubectl delete deployment <name>` | 🗑️ Delete a deployment |

---

## 🌐 Services & Networking

| Command | Description |
|--------|-------------|
| `kubectl get svc` | 📋 List services |
| `kubectl expose deployment <name> --port=80 --type=ClusterIP` | 🔌 Expose a deployment as a service |
| `kubectl describe svc <svc>` | 🔍 Detailed service info |
| `kubectl get ingress` | 🌍 List ingress resources |
| `kubectl get endpoints` | 🎯 List service endpoints |

---

## 🗂️ Namespaces & Config

| Command | Description |
|--------|-------------|
| `kubectl get namespaces` | 📋 List namespaces |
| `kubectl create namespace <name>` | 🆕 Create a namespace |
| `kubectl delete namespace <name>` | 🧹 Delete a namespace |
| `kubectl config set-context --current --namespace=<ns>` | 🔀 Switch default namespace |
| `kubectl get configmap` | 📄 List ConfigMaps |
| `kubectl get secrets` | 🔐 List Secrets |
| `kubectl create secret generic <name> --from-literal=key=value` | 🆕 Create a Secret |

---

## 📄 Apply & Manage Manifests

| Command | Description |
|--------|-------------|
| `kubectl apply -f <file.yaml>` | ✅ Create/update resources from a manifest |
| `kubectl apply -f <dir>/` | 📁 Apply all manifests in a directory |
| `kubectl delete -f <file.yaml>` | 🗑️ Delete resources defined in a manifest |
| `kubectl diff -f <file.yaml>` | 🔍 Preview changes before applying |
| `kubectl edit deployment <name>` | ✏️ Edit a live resource |
| `kubectl explain <resource>` | 📘 Show resource field documentation |

---

## 💾 Volumes & Storage

| Command | Description |
|--------|-------------|
| `kubectl get pv` | 💾 List PersistentVolumes |
| `kubectl get pvc` | 📋 List PersistentVolumeClaims |
| `kubectl describe pvc <name>` | 🔍 Detailed PVC info |
| `kubectl get storageclass` | 🗄️ List StorageClasses |

---

## 🔄 Cluster Maintenance

| Command | Description |
|--------|-------------|
| `kubectl get events` | 📰 Show recent cluster events |
| `kubectl top nodes` | 📈 Show node resource usage (needs metrics-server) |
| `kubectl top pods` | 📈 Show pod resource usage |
| `kubectl drain <node>` | 🚧 Safely evict pods from a node |
| `kubectl cordon <node>` | 🔒 Mark node as unschedulable |
| `kubectl uncordon <node>` | 🔓 Mark node as schedulable again |
| `kubectl taint nodes <node> key=value:NoSchedule` | 🏷️ Taint a node |

---

## 🧠 Tip

💡 Use `--help` with any `kubectl` command to learn more, e.g.:

```bash
kubectl get pods --help
```

---

> ✅ Keep this README as a reference for your Kubernetes journey. Contributions welcome!
> ⭐ Star this repo if you found it helpful!
