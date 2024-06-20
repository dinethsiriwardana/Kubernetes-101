To perform a rolling update for the `nginx-deployment` deployment to use the new `nginx:1.19` image, follow these steps:

1. **Edit the deployment to update the image**:
   ```bash
   kubectl edit deployment nginx-deployment
   ```
   In the editor, change the image for the container from `nginx:1.16` to `nginx:1.19`. Look for the section under `spec.template.spec.containers` and update the `image` field:
   ```yaml
   spec:
     containers:
     - name: nginx-container
       image: nginx:1.19
   ```

2. **Save and exit the editor**:
   After updating the image, save the file and exit the editor (for `vi`, this is done by pressing `Esc`, typing `:wq`, and pressing `Enter`).

3. **Verify the update is being rolled out**:
   ```bash
   kubectl rollout status deployment/nginx-deployment
   ```
   This command will show the rollout status and ensure the new pods are being created successfully.

4. **Check the status of the deployment**:
   ```bash
   kubectl get deployment nginx-deployment
   ```
   Example output:
   ```
   NAME               READY   UP-TO-DATE   AVAILABLE   AGE
   nginx-deployment   3/3     3            3           4m2s
   ```

5. **Verify the status of the pods**:
   ```bash
   kubectl get pods
   ```
   Example output:
   ```
   NAME                               READY   STATUS    RESTARTS   AGE
   nginx-deployment-dc49f85cc-c7k97   1/1     Running   0          51s
   nginx-deployment-dc49f85cc-mlvhl   1/1     Running   0          43s
   nginx-deployment-dc49f85cc-xljgd   1/1     Running   0          41s
   ```

6. **Describe one of the pods to ensure it uses the new image**:
   ```bash
   kubectl describe pod <pod-name>
   ```
   Replace `<pod-name>` with the name of one of the pods from the previous `kubectl get pods` output. Verify the image is `nginx:1.19`.

   Example:
   ```bash
   kubectl describe pod nginx-deployment-dc49f85cc-c7k97
   ```

   Key output to check:
   ```
   Containers:
     nginx-container:
       Image:          nginx:1.19
   ```

These steps will ensure that the `nginx-deployment` is updated to use the `nginx:1.19` image and that all pods are operational post-update.

[[6 Revert Deployment to Previous Version in Kubernetes]]