To roll back the `nginx-deployment` to the previous revision, you can use the following steps:

1. **Check the current deployment status**:
   ```bash
   kubectl get deployments
   ```

2. **Get the rollout history of the deployment**:
   ```bash
   kubectl rollout history deployment nginx-deployment
   ```

3. **Rollback the deployment to the previous revision**:
   ```bash
   kubectl rollout undo deployment nginx-deployment --to-revision=1
   ```

4. **Check the status of the rollback**:
   ```bash
   kubectl rollout status deployment nginx-deployment
   ```

5. **Verify the deployment and pods status**:
   ```bash
   kubectl get deployments
   kubectl get pods
   ```

6. **Describe the deployment to ensure it has rolled back to the correct revision**:
   ```bash
   kubectl describe deployment nginx-deployment
   ```

Here are the detailed steps executed in sequence:

```bash
# Step 1: Check the current deployments
kubectl get deployments

# Step 2: Get the rollout history of the deployment
kubectl rollout history deployment nginx-deployment

# Step 3: Rollback to the previous revision
kubectl rollout undo deployment nginx-deployment --to-revision=1

# Step 4: Check the status of the rollback
kubectl rollout status deployment nginx-deployment

# Step 5: Verify the deployment and pods status
kubectl get deployments
kubectl get pods

# Step 6: Describe the deployment to confirm the rollback
kubectl describe deployment nginx-deployment
```

This will ensure the `nginx-deployment` is rolled back to the previous version, and all pods are operational.

[[7 Deploy Replica Set in Kubernetes Cluster]]