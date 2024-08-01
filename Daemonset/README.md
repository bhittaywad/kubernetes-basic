# Daemonset
A DaemonSet in Kubernetes is a type of workload resource that ensures a copy of a specified pod runs on all (or some) nodes in a cluster. DaemonSets are particularly useful for running system-level services that need to be present on every node, such as monitoring agents, logging daemons, or network proxies.
# Key Features and Characteristics of DaemonSets
## Uniform Deployment: 
A DaemonSet automatically schedules a pod on all or specific nodes when they join the cluster, ensuring that the application runs consistently across the nodes.

## Automatic Scaling: 
As new nodes are added to the cluster, the DaemonSet controller automatically schedules the specified pods on these new nodes. Conversely, when nodes are removed, the pods are also terminated.

## Targeted Node Deployment: 
DaemonSets can be configured to deploy pods only on certain nodes using node selectors, affinity rules, or tolerations. This feature allows you to target specific groups of nodes, such as those with specific hardware or in certain geographical locations.

## Rolling Updates: 
DaemonSets support rolling updates, allowing you to update the daemonized application across all nodes in a controlled and automated manner. This ensures that there is minimal disruption to the service.

## Single Pod per Node: 
A DaemonSet guarantees only one pod replica per node. This is different from other controllers like Deployments or ReplicaSets, which can schedule multiple replicas of a pod across the cluster.
## Common Use Cases for DaemonSets
## Logging and Monitoring Agents:
 Deploying agents that collect logs or metrics from all nodes.
## Node Proxies: 
Running network proxies, such as CNI plugins, which need to be present on every node.
## Security Agents: 
Deploying security agents that monitor and protect the system integrity of each node.
Node Configuration Management: Distributing and managing configuration files or other node-level services.


