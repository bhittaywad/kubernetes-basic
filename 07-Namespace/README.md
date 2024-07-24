# what is namespace
A Kubernetes namespace is a way to divide cluster resources between multiple users or teams. It provides a scope for names within the cluster, allowing for more efficient organization and management of resources.
## Resource Isolation:
Namespaces provide a mechanism to isolate resources within the same cluster. This means different teams or projects can have their own resources without interfering with each other.
## Resource Quotas:
Administrators can set resource quotas on namespaces to limit the amount of resources (CPU, memory, etc.) that can be consumed, ensuring fair usage across different namespaces.
## Access Control:
Role-Based Access Control (RBAC) policies can be applied to namespaces, allowing for granular permissions and access control for different users and teams.

# Creating and Using Namespaces
## Creating a Namespace
ou can create a namespace using the kubectl command or by defining it in a YAML file.
kubectl create namespace my-namespace
## Using Namespaces
To work within a specific namespace, you can specify the namespace in your kubectl commands using the -n flag.
# Example
kubectl get pods -n my-namespace

kubectl create deployment nginx --image=nginx -n my-namespace

kubectl get namespaces



