# Docker Environment for Kubernetes & DevOps Tools

This Dockerfile builds a **development environment** tailored for Kubernetes, DevOps, and cloud-native workflows. It includes all essential CLI tools, SDKs, and utilities you need for deploying, managing, and scaling containerized applications.

---

## 🛠 What's Included

The Docker image installs:

- **Base system:** Ubuntu with essential utilities (`bash`, `vim`, `git`, `curl`, `wget`, `jq`, `screen`, `uuid-runtime`, etc.)
- **Docker CLI**: `docker`, `docker-compose`, `docker-buildx`
- **AWS CLI v2**: Manage AWS resources
- **Terraform**: Infrastructure-as-Code automation
- **Kubernetes tools**: `kubectl`, `kustomize`, `kubetail`, `kops`, `kubectl-argo-rollouts`
- **Helm**: Package management for Kubernetes
- **Step CLI**: For certificate management
- **Linkerd Enterprise**: Service mesh for microservices
- **Shell enhancements**: bash-completion, aliases, and Kubernetes CLI autocompletion

# How to run & build the docker image
## Login
docker login -u <username> -p <password>

## Run
```
# configure docker-compose.yml if you have anything special on your local
docker-compose up -d
docker exec -it k8s bash
```

## Build
```
# k8s-client
docker build -f ./k8s-client.df -t gloryluo/k8s-client:1.31.0.0 ./
docker push intellibank/k8s-client:1.31.0.0
```
