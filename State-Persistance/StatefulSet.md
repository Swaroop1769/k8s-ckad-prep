Stateful Sets are similar to Deployment sets as in they create PODs based on template
Stateful Sets can:
- Can scale up and scale down

- Can perform rolling updated and rollbacks

Differences wrt deployment sets are:

- PODs are create in a sequential order
 - after a pod is deployed it has to be ready and in running state before next POD is deployed.

### Stateful sets assign a unique original index to each POD, a number starting from 0 from from pod and increments by one

- Stateful sets maintain a **Sticky identiy** for each of their PODs and these help with remaining steps.

Just the kind changes to StatefulSet and also mention **serviceName** in yml file

1. Ordered, graceful deployment
2. Stable, unique network identifier(DNS record)


## Headless Service

A headless service is created like a normal service but it does not have an IP of its own. 
It does not perform any loadbalancing

All it does is create DNS entries fro each pod, using pod name and a subdomain




