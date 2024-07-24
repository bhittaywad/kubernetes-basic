 # what is Ingress
 what is kubernetes ingress
Kubernetes Ingress is a resource used to manage external access to services within a Kubernetes cluster, typically HTTP and HTTPS traffic. It provides a way to define rules for routing external traffic to the appropriate services within the cluster
## Ingress Resource:
A collection of rules that allow inbound connections to reach the cluster services. These rules define how to route external HTTP/HTTPS traffic to specific services based on the request paths or hostnames.

# Benefits of Using Ingress
#### Centralized Traffic Management: Provides a central point to manage external traffic, simplifying the configuration of routing rules and load balancing. 
#### Path-Based and Host-Based Routing: Supports routing traffic based on URL paths and hostnames, allowing for more flexible and granular control.  
#### SSL/TLS Termination: Can handle SSL/TLS termination, offloading this task from backend services. 
# Steps to Use Ingress
## 1-Deploy an Ingress Controller:
Before using Ingress resources, you need to deploy an Ingress Controller in your Kubernetes cluster. The Ingress Controller is responsible for fulfilling the Ingress rules.

Example for deploying the NGINX Ingress Controller:

kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/main/deploy/static/provider/cloud/deploy.yaml
## 2-Create Ingress Resources:

Define Ingress resources that specify the routing rules for your applications.

Apply the Ingress resource using kubectl:

kubectl apply -f example-ingress.yaml








