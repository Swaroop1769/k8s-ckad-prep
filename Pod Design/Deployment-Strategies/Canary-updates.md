# Canary Strategy

In this strategy a new version is deployed and route a small percentage of traffic to it.

Majority of traffic routed to older version

# In kubernetes Native way it's achieved as follows

1. Routes traffic to both versions
2. Route a small percentage of traffic to version 2

limitation in Canary Deployment with Kubernetes and deployment services:
- limited control over the split of traffic between each deployment.

### traffic split is always governed by the number of pods present in each deployment.

