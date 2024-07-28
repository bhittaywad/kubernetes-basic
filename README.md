 # Repo to learn Kubernetes with examples. Contributions are most welcome.
 # # Kubernetes Learning Guide

This repository serves as a guide for learning Kubernetes, a powerful open-source system for managing containerized applications across a cluster of machines.

## Table of Contents

- [Introduction to Kubernetes](https://github.com/bhittaywad/kubernetes-basic/tree/main/01-kubernetes-intro%20%26%20architecture)
- [What is pod](https://github.com/bhittaywad/kubernetes-basic/tree/main/02-Pod)
- Kubernetes component
- replica-set
- Deployment
- deployment startigies
- Service
- service type
- Namespace
- kubernetes volume
- type of volume (pv,pvc,storage class)
- Configmap # secret
- 
- [License](#license)

## Introduction

Kubernetes, also known as K8s, is a system designed to automate the deployment, scaling, and operation of application containers. It was originally designed by Google and is now maintained by the Cloud Native Computing Foundation (CNCF).

## Getting Started

To start learning Kubernetes, you need to have a basic understanding of Docker and containerization concepts. Here are the initial steps:

1. **Install Docker**: [Docker Installation Guide](https://docs.docker.com/get-docker/)
2. **Install Kubernetes**: [Kubernetes Installation Guide](https://kubernetes.io/docs/setup/)

You can also use a local Kubernetes setup with tools like Minikube or Kind:
- [Minikube](https://minikube.sigs.k8s.io/docs/start/)
- [Kind](https://kind.sigs.k8s.io/docs/user/quick-start/)

## Kubernetes Components

Understanding the core components of Kubernetes is essential:

- **Master Node**: Manages the Kubernetes cluster. Key components include:
  - **API Server**: Frontend for the Kubernetes control plane.
  - **Controller Manager**: Handles controllers that regulate the state of the cluster.
  - **Scheduler**: Assigns workloads to nodes.
  - **etcd**: Stores all cluster data.
  
- **Worker Nodes**: Run containerized applications. Key components include:
  - **Kubelet**: Ensures containers are running in a pod.
  - **Kube-proxy**: Manages network rules.
  - **Container Runtime**: Software that runs the containers (e.g., Docker, containerd).

## Basic Concepts

Here are some fundamental concepts you need to understand:

- **Pod**: The smallest deployable unit in Kubernetes.
- **Service**: An abstraction that defines a logical set of Pods and a policy by which to access them.
- **Deployment**: A higher-level abstraction that manages Pods and ReplicaSets.
- **ConfigMap and Secret**: Manage configuration data and sensitive information for applications.
- **Namespace**: A way to divide cluster resources between multiple users.
- **Volume**:
Kubernetes volumes provide a way for containers in a Pod to access shared storage. Volumes are crucial for persisting data, sharing data between containers, and enabling data access across different nodes.

## Types of Volumes

1. **emptyDir**: Temporary storage that is created when a Pod is assigned to a node and exists as long as that Pod is running on that node.

2. **hostPath**: Mounts a file or directory from the host node’s filesystem into your Pod.

3. **gcePersistentDisk**: Mounts a Google Compute Engine Persistent Disk into your Pod.

4. **awsElasticBlockStore**: Mounts an AWS Elastic Block Store volume into your Pod.

5. **nfs**: Mounts an NFS (Network File System) share into your Pod.

6. **persistentVolumeClaim**: Uses a PersistentVolumeClaim to mount a PersistentVolume into your Pod.

7. **configMap**: Provides a way to inject configuration data into Pods.

8. **secret**: Provides a way to pass sensitive information, such as passwords, into your Pod.


## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
