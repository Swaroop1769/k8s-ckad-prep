Different stages in lifecycle of a Pod:
Pod has Pod Status and Pod Conditions

When a pod is first created it's in **Pending** state - scheduler tries to figure out where to place pod. If scheduler is unable to find node - it remains in pending state

Once when pod is scheduled, it goes to **ContainerCreating** status
then goes to **Running** State

### Pod Conditions
Conditions complement pod status - an array of true or false values that tell us state of a Pod

1. when pod scheduled on a node --> **PodScheduled** condition is set to **True**
2. when pod is initialized, it's value is set to true 
3. multiple containers in pod - if all are ready - **ContainerReady** condition is set to **True**

The ready conditions indicate that app inside pod is running and is ready to **accept user traffic**

tie the ready condition to the actual state of application inside the container -----
Readiness Probes:
There are different ways that can define if an application inside a container is actually ready....can do the appropritate tests or attach probes

- in case of web app (HTTP test - /api/ready)
- in case of database (TCP test - 3306)
- simply run the exec command inside container to see if app is ready...



