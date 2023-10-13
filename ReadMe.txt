This is a configuration to deploy a simple web-app in a kubernetes cluster
1. Create a Persist Volume, accessmode is RWO, storage class is manual, volume type is hostPath and capacity if 5Gi
2. Create a Persist Volume Claim to request 1Gi storage, accessmode is RWO and storage class set to manual
Create a pod with image set to nginx:latest, and the PV mounted at the root of the webserver
Create service of the type nodePort configure to 30008