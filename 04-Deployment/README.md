# what is Deployment ?
A Deployment is a higher-level Kubernetes resource that manages ReplicaSets and provides declarative updates to applications. It offers several advanced features for managing applications, such as rolling updates, rollbacks, and scaling. Deployments simplify the process of managing application updates and ensuring the desired state of the application
# Key Features of Deployment
Deployments allow you to define the desired state of your application, including the number of replicas, the container image to use, and other settings. Kubernetes then ensures that the actual state matches the desired state.

 ### Rolling Updates:

Deployments support rolling updates, which gradually update pods with new versions of the application without downtime. This ensures that the application remains available during updates.

 ### Rollbacks:

If an update fails or causes issues, Deployments allow you to roll back to a previous version. This helps maintain application stability and reliability.

 ### Scaling:

Deployments enable easy scaling of applications by adjusting the number of replicas. This can be done manually or automatically using the Horizontal Pod Autoscaler.

 ### Self-Healing:

Deployments automatically replace failed or terminated pods, ensuring that the desired number of replicas is always running.

 ### Multiple Strategies:

Deployments support different update strategies, such as rolling updates and recreate strategies, allowing you to choose the best approach for your application.
# Deployment Strategies?

1-Rolling update

2-recreate

3-canery deployment

# Rolling Update:

Gradually replaces old pods with new ones. This is the default strategy and minimizes downtime.

# Recreate:

Terminates all existing pods before creating new ones. This strategy can cause downtime but ensures that no old pods are running

# canary deployment:

A canary deployment is a deployment strategy that releases a new version of an application to a small subset of users before rolling it out to the entire infrastructure. This approach allows developers to test new features in a production environment and monitor their performance and impact on a limited scale, reducing the risk of widespread issue.

