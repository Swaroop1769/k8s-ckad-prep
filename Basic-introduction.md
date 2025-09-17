Kubernetes is Container Orchestration Technology
K8 Architecture: 
//Node: A node is a physical or virtual machine on which K8 is installed.
A node is a worker machine where all the containers are launched by K8. Also known as minions in past.

Cluster: is a set of nodes grouped together. In this way even if one node fails, the application is still accessible from other nodes.
Having multiple nodes helps in sharing load as well.

Who is responsible for managing cluster? where is information about members of cluster stored? How are nodes monitored? When a node fails how the workload of failed node is moved to another worker node?

///MASTER///
The master node has k8 installed on it and watches the nodes in the cluster and is responsible for the actual orchestration of containers on the worker nodes.

When K8 is installed on system we are installing the following components:

An API Server
An etcd service
a kubelet service
a container runtime
controllers
Schedulers

//API Server// acts as frontend for K8. The users, management devices, command line interfaces all talk to API Server to interact with K8 cluster.

//etcd key store// is a distributed reliable key value store used by K8 to store all data used to manage the cluster.

etcd is responsible for implementing locks within the cluster to ensure that there are no conflicts between the Masters.

//Scheduler// is responsible for distributing work or containers across multiple nodes. It looks for newly created containers and assigns them to nodes.

//Controllers// are the brain behind the orchestration. Responsible for noticing and responding when nodes, containers or end points goes down. Controllers make decisions to bring up new containers in such cases.

//Container Runtime// is underlying software used to run containers.(docker in this case)

//Kubelet// is the agent that runs on each node in the cluster. Agent is responsible for making sure that the containers are running on the nodes as expected.

Master vs Worker(Slave) Nodes:

How does on server become a master and the other the slave?

1. Worker node - where the containers are hosted. and to run docker container on a system, we need a container runtime installed

3. worker node has kubelet agent that is responsible for interacting with a master - to provide health information of worker node and carry out actions requested by the Master on the worker nodes.

4. All the info gathered are stored in a key value store on the master - key value store is based on the ///etcd///framework

5. The Master node also has the controller and Scheduler

2. The Master server has the kube API server and that is what makes it a master.


//Kubectl//: command line tool or kube control

kubectl tool is used to deploy and manage applications on a K8 cluster - to get cluster information, to get status of other nodes in the cluster

//// kubectl run ///// command is used to deploy an application on the cluster

//// kubectl cluster info //// command is used to view info about the cluster.
