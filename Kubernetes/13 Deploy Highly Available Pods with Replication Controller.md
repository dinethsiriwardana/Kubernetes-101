The ReplicationController `nginx-replicationcontroller` has been successfully created with the specifications provided. Here's the YAML configuration and the steps followed:

```yaml
apiVersion: v1
kind: ReplicationController
metadata:
  name: nginx-replicationcontroller
spec:
  replicas: 3
  selector:
    app: nginx_app
    type: front-end
  template:
    metadata:
      labels:
        app: nginx_app
        type: front-end
    spec:
      containers:
      - name: nginx-container
        image: nginx:latest
```

Steps followed:
1. Created a YAML file `rc.yaml` with the above configuration.
2. Applied the configuration using `kubectl create -f rc.yaml`.
3. Verified the ReplicationController was created successfully using `kubectl get rc`.
4. Checked the status of the pods created by the ReplicationController using `kubectl get pods`.

All pods (`nginx-replicationcontroller-2drhk`, `nginx-replicationcontroller-clmtb`, `nginx-replicationcontroller-n47gw`) are in the `Running` state, confirming the setup meets the requirement for a highly available infrastructure with three pods of nginx running.


Reference https://kubernetes.io/docs/concepts/workloads/controllers/replicationcontroller/


[[11 Resolve Pod Deployment Issue]]