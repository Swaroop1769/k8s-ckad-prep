## types of traffic
- Ingress  (Incoming traffic from users is Ingress traffic)
- Egress (outgoing request to the app server is egress traffic)

## Network Security in K8s

-- in K8s whatever we implement, the pods should be able to communicate with each other without having to configure any additional settings like routes

- By default K8s is configured with an **All Allow** rule - that allows traffic from any pod to any other pod or services within the cluster



## Network Policy

is an object in Kubernetes namespace, just like pods, replicasets or services

We can link a Network policy to one or more pods.

-- Define Rules within Network Policy
Network policy flow will be something like with an example:

Allow --> Ingress Traffic --> From API Pod ----on--> Port 3306



