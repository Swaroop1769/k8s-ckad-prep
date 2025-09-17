Before even the PV is created, we must create the disk on cloud and then manually create PV - this is called **Static Provisioning**

- So comes the Storage Classes for **Dynamic Provisioning**

- can create a storage class definition file 

- once when we create this sc-definition file we no longer need the PV definition as PV and any associated storage is going to be created automatically when storage class is created.

- for PVC to use storage class that's defined in sc-definition.yaml, we specify the storageClassName in PVC definition

