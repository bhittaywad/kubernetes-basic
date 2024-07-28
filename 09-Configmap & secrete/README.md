












# what is Configmap
ConfigMaps in Kubernetes are used to manage configuration data for your applications. They allow you to decouple configuration artifacts from image content to keep containerized applications portable.
apiVersion: v1
kind: ConfigMap
metadata:
  name: my-config
  namespace: my-namespace
data:
  database_url: "jdbc:postgresql://db-service:5432/mydatabase"
  log_level: "INFO"
  ## Applying the ConfigMap
  kubectl apply -f configmap.yaml

## Deployment YAML Using ConfigMap
Here’s an example of a Deployment that uses the ConfigMap

apiVersion: apps/v1
kind: Deployment
metadata:
  name: blue-application
  namespace: my-namespace
spec:
  replicas: 3
  selector:
    matchLabels:
      app: blue-app
  template:
    metadata:
      labels:
        app: blue-app
    spec:
      containers:
      - name: blue-app-container
        image: my-blue-app:latest
        ports:
        - containerPort: 8080
        env:
        - name: DATABASE_URL
          valueFrom:
            configMapKeyRef:
              name: my-config
              key: database_url
        - name: LOG_LEVEL
          valueFrom:
            configMapKeyRef:
              name: my-config
              key: log_level












# What is a Secret?
A Secret is an object that contains a small amount of sensitive data such as a password, a token, or a key. Such information might otherwise be put in a Pod specification or in a container image. Using a Secret means that you don’t need to include confidential data in your application code.

## Creating a Secret
You can create a Secret from a file, literal values, or with a YAML definition.

## Example: Creating a Secret from Literal Values

# Using a Secret in a Pod
apiVersion: v1
kind: Pod
metadata:
  name: my-pod
spec:
  containers:
  - name: my-container
    image: nginx
    env:
    - name: USERNAME
      valueFrom:
        secretKeyRef:
          name: my-secret
          key: username
    - name: PASSWORD
      valueFrom:
        secretKeyRef:
          name: my-secret
          key: password

    
