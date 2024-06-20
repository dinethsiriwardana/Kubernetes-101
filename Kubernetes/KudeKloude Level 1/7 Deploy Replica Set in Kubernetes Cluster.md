To create the desired ReplicaSet, you can follow these steps:

Reference :- 
https://kubernetes.io/docs/concepts/workloads/controllers/replicaset/

1. **Generate the YAML for the ReplicaSet**:
    ```bash
    kubectl create deployment nginx-replicaset --image=nginx:latest --dry-run=client -o yaml > replicaset.yaml
    ```

2. **Edit the generated YAML** to match the required specification. Here is the corrected YAML content:

    ```yaml
    apiVersion: apps/v1
    kind: ReplicaSet
    metadata:
      name: nginx-replicaset
      labels:
        app: nginx_app
        type: front-end
    spec:
      replicas: 4
      selector:
        matchLabels:
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

3. **Apply the YAML file** to create the ReplicaSet:

    ```bash
    kubectl apply -f replicaset.yaml
    ```

4. **Verify the creation of the ReplicaSet**:

    ```bash
    kubectl get replicaset
    ```

5. **Describe the ReplicaSet** to ensure it is running as expected:

    ```bash
    kubectl describe replicaset nginx-replicaset
    ```

By following these steps, you will create a ReplicaSet named `nginx-replicaset` with the desired configuration.

[[8 Schedule Cronjobs in Kubernetes]]