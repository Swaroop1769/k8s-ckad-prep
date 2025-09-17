## Persistant Volume Claims

Persistant volumes and Persistant Volume claims are 2 separate objects in K8s

An Admin creates **persistant volumes**

A user create **Persistant Volume Claims**  to use the storage

once the PVC's are created K8s binds the PVs based on requests and properties set on volumes.

There's one-to-one relationship between claims and volumes!!

## Documentation URL

https://kubernetes.io/docs/concepts/storage/persistent-volumes/#claims-as-volumes


