## Definition:
 Labels are key-value pairs attached to Kubernetes objects, such as pods, services, nodes, and more. They provide metadata that can be used to identify and group resources.
## Purpose:
 Labels are used to organize and select subsets of objects. They are not inherently meaningful but are used by selectors to group objects for various operations like scaling, rolling updates, or load balancing.
## Format:
 Labels are key-value pairs, with keys and values both being strings. Example: env=production, app=nginx.