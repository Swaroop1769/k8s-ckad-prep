## Helm


- Helm is often called a **package manager** for kubernetes.
- with install or uninstall wizard, and a release manager helping us upgrade or roll back application

## Core thing is that Helm lets us treat the kubernetes apps as apps instead of collection of Objects.

Helm looks at objects( in K8s application - services,secret,PVC,PV,Deployemt) as part of big package as a group.

- eg: think of a computer game and it's executables 

Helm is quite advantageous 

- helm install wordpress

Instead of editting or modifying multiple files we can declare every custom setting in a single**values.yaml** file 

### with single command we can upgrade the application

- helm upgrade wordpress

rollback to older version 
- helm rollback wordpress

single command to uninstall app
- helm uninstall wordpress


### Helm Concepts

- all the yaml files like deployment.yaml/pv.yaml/service.yaml/secret.yaml/pvc/yaml all these together combine forms an K8s application.
- in above mentioned files, simply replace one line:
Image: {{ .Values.image}} //deployment.yaml
key: {{.Values.passwordEncoded}} //secret.yaml
storage: {{.Values.storage}} //pvc.yaml
storage: {{.Values.storage}}  //pv.yaml


- Fetching all these values from another place - **values.yaml**

## A combination of templates + Values.yaml --> final version of definition files that can be used to deploy app in k8s cluster

### Together templates + values file forms **HELM CHARTS**

- A single helm chart maybe used to deploy a simple app like wordpress(example)

- https://artifacthub.io - it's like a repo where users upload helm charts which we can make use of

- helm search hub wordpress //command

The Artifact hub is community driven chart repository - other repos are - **bitnami Helm repository**
### for bitnami repo:
- helm repo add bitnami https://charts.bitnami.com/bitnami


- helm search repo wordpress
- helm repo list
- helm install [release-name] [chart-name]


