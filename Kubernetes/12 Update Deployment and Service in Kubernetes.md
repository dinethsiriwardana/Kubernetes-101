To update the existing `nginx-deployment` and `nginx-service` with the specified changes, 

1. Modify the service nodeport from 30008 to 32165

2. Change the replicas count from 1 to 5

3. Update the image from nginx:1.18 to nginx

follow these steps:

1. **Modify the NodePort of the Service**:
    ```bash
    kubectl edit svc nginx-service
    ```
    Change the NodePort from `30008` to `32165`:
    ```yaml
    spec:
      ports:
        - port: 80
          protocol: TCP
          targetPort: 80
          nodePort: 32165
    ```

2. **Change the Replicas Count**:
    ```bash
    kubectl edit deployment nginx-deployment
    ```
    Update the replicas count from `1` to `5`:
    ```yaml
    spec:
      replicas: 5
    ```

3. **Update the Image**:
    While editing the same deployment, change the image from `nginx:1.18` to `nginx:latest`:
    ```yaml
    spec:
      containers:
      - name: nginx-container
        image: nginx:latest
    ```

After making these changes, verify that they have been applied correctly:

- **Check Deployment Status**:
    ```bash
    kubectl get deploy nginx-deployment
    ```

- **Describe Deployment** to confirm the details:
    ```bash
    kubectl describe deploy nginx-deployment
    ```

- **Check Pods** to ensure all replicas are running:
    ```bash
    kubectl get pods
    ```

- **Check Service** to confirm the NodePort change:
    ```bash
    kubectl get svc nginx-service
    ```

Following these steps ensures the deployment and service are updated without deleting them, implementing the necessary changes effectively.


[[12 Update Deployment and Service in Kubernetes]]