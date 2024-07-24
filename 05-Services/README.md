# what is service?
In Kubernetes, a Service is an abstraction that defines a logical set of Pods and a policy by which to access them. Services enable network access to a dynamic set of Pods and facilitate load balancing, discovery, and communication between different parts of an application.
type of service:

 ## 1-ClusterIP (default):

Exposes the Service on a cluster-internal IP. The Service is only accessible within the cluster.

## 2-Node-Port:

Exposes the Service on each Node’s IP at a static port. This allows external traffic to access the Service via <Node-IP>:<Node-Port>.

## 3-Load-Balancer:

Exposes the Service externally using a cloud provider's load balancer. The cloud provider manages an external IP address that forwards traffic to the Service.
