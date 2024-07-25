# what is Pod ?
A Pod is the smallest and simplest unit in the Kubernetes object model that you can create or deploy. It represents a single instance of a running process in your cluster and can contain one or more containers, such as Docker containers

## Single or Multiple Containers:

  1-Single Container Pod: The most common use case, where each Pod runs a single container.
  2-Multi-Container Pod: Contains multiple containers that need to work closely together. These containers share the same network namespace, meaning they can communicate with each other using localhost
 3-Shared Resources:

Network: All containers within a pod share the same IP address and port space. They can communicate with each other using localhost.

Storage: Pods can specify a set of shared storage volumes that can be mounted into the individual containers. This allows containers to share data.

Namespace: Pods share namespaces like PID (process ID), IPC (inter-process communication), and others
