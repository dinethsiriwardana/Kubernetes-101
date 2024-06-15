Steps to create a pod named `httpd-pod` with specified resource limits and requests:

1. **Generate the pod configuration with a dry run**:
   ```bash
   kubectl run httpd-pod --image=httpd:latest --dry-run=client -o yaml > pod.yaml
   ```

2. **Edit the `pod.yaml` file**:
   Open `pod.yaml` in your preferred text editor, such as `vi`:
   ```bash
   vi pod.yaml
   ```

3. **Modify the `pod.yaml` file to include resource requests and limits**:
   Update the `pod.yaml` file to look like this:
   ```yaml
   apiVersion: v1
   kind: Pod
   metadata:
     creationTimestamp: null
     labels:
       run: httpd-pod
     name: httpd-pod
   spec:
     containers:
     - image: httpd:latest
       name: httpd-container
       resources:
         requests:
           memory: "15Mi"
           cpu: "100m"
         limits:
           memory: "20Mi"
           cpu: "100m"
     dnsPolicy: ClusterFirst
     restartPolicy: Always
   status: {}
   ```

4. **Create the pod using the modified configuration**:
   ```bash
   kubectl create -f pod.yaml
   ```

5. **Verify the pod is created and running**:
   ```bash
   kubectl get pod
   ```

Example Output:
```
NAME        READY   STATUS    RESTARTS   AGE
httpd-pod   1/1     Running   0          15s
```

These steps will create a pod named `httpd-pod` with the specified resource requests and limits, ensuring efficient resource utilization.

[[5 Execute Rolling Updates in Kubernetes]]