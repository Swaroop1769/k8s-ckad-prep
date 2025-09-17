Kubernetes services enable communication between various components within and outside application.

Services enable communication between Front-end application and end users AND front-end and backend communication AND even external data source communication (database)

### Services enable loose coupling between microservices in application


## Networking

External Communication

K8s Service is an object just like a Pod, ReplicaSet or Deployments

Service listens to a port on the node and forward request to the pods - this type is **Node Port**

### Service Types

- **Node Port** (service makes an internal pord accessible on a port on the node. )
- **Cluster IP** (the service created virtual IP inside the cluster to enable communication between different services, such as a set of front-end servers to a set of backend-servers )

    - cannot rely on IP addressess for internal communication between application. A k8s service helps to group the pods together and provide a single interface to access pods in a group 
- **Load Balancer Type** ( it provisions a load balancer for our application in supported cloud providers.)
