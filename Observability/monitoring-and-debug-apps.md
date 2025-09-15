# Monitoring Kubernetes

How can resource consumption be monitored on K8s?
or what can we monitor?
1. Node level metrics (number of nodes in Cluster, how many are healthy)
2. Performance Metrics (CPU, Memory, Network, Disk Utlization)
3. Pod Level metrics (no. of pods, performance metrics of each pod)

Monitoring Solutions - Metrics Server, Prometheus, Elastic Stack, DataDog, Dynatrace

Metrics Server - rectrives metrics from each k8 nodes and pods, aggregrates them and stores them in memory. 

## Metrics Server is an In-Memory monitoring Solution and doesn't store metrics on the disk


Kubernetes runs an agent on each node, called **Kubelet** - responsible for receiving instructions from K8s API master server and running pods on nodes.


**Kubelet** also contains a sub-component called **cAdvisor** or **Container Advisor** - responsible for retriving performance metrics from pods and exposing them through Kubelet API to make the metrics available for Metrics Server.

## If using a minikube:

''
minikube addons enable metrics-server
''
## others

''
git clone https://github.com/kubernetes-incubator/metrics-server

kubectl create -f deploy/1.8+/
''

right after enabling this give some time to collect the metrics and then give the following command:

''
kubectl top node
''

''
kubectl top pod
''