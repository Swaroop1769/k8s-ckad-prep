# KubeConfig

- Instead of always passing the kubectl commands we can make a kubeconfig file and give all the parameters there.

- By default, the kubectl tool looks for a file named **config** under a directory **"$HOME/.kube/config"**

Kubeconfig file has 3 sections:
1. Clusters (multiple clusters for dev/prod environments)
2. Users (user accounts with which we can access the clusters - admin user/dev/prod users)
3. Contexts (define which user account will be used to access which cluster eg: Admin@production)



