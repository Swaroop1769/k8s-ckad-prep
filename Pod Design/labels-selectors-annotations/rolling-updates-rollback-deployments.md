## Rollouts and Versioning in a Deployment

when a deployment is created it first triggers a rollout. 
A new rollout creates a new Deployment revision.(Revision 1)

again a new rollout creates a new revision

- in k8s we can use following command:
'''
kubectl rollout status deployment/my-app-deployment
'''
- gives us revisions and history of deployment
''
kubectl rollout history deployment/my-app-deployment
''

###there are 2 types of Deployment Strategies:
1. **Recreate Strategy** - delete older version containers and then create new version container with later versions

this isn't the default strategy as it will cause the **application to be down**

2. **Rolling Update** - take down the older version and bring up newer version one by one, this way the app never goes down

Rolling Update is the default deployment strategy.

to undo a change in the rollout of a deployement - like if we want to move back to earlier revision

''
kubectl rollout undo deployment/my-app-deployment
''
# Commands Summary
**Create** - '''kubectl create -f deployment-definition.yaml'''
**Get** - kubectl get deployments
**Update:**
-  kubectl apply -f deployment-definition.yaml
- kubectl set image deployment/myapp-deployment nginx=nginx:1.9.1

**Status:**
- kubectl rollout status deployment/myapp-deployment
- kubectl rollout history deployment/my-deployment

**Rollback** - kubectl rollout deployment/my-deployment
