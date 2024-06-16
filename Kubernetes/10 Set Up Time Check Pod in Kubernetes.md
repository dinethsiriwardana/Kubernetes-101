Follow these steps to create a time check pod.

1. **Create the ConfigMap** to store the environment variable `TIME_FREQ`.

    ```bash
    vi configmap.yaml
    ```

    Add the following content to `configmap.yaml`:

    ```yaml
    apiVersion: v1
    kind: ConfigMap
    metadata:
      name: time-config
      namespace: datacenter
    data:
      TIME_FREQ: "12"
    ```

    Save and close the file. Then, create the ConfigMap:

    ```bash
    kubectl create -f configmap.yaml
    ```

    This step creates a ConfigMap named `time-config` in the `datacenter` namespace with the key-value pair `TIME_FREQ: 12`  .

2. **Create the Pod** with the specified configuration.

    ```bash
    vi pod.yaml
    ```

    Add the following content to `pod.yaml`:

    ```yaml
    apiVersion: v1
    kind: Pod
    metadata:
      name: time-check
      namespace: datacenter
    spec:
      containers:
      - name: time-check
        image: busybox:latest
        command: ["sh", "-c", "while true; do date; sleep $TIME_FREQ; done >> /opt/finance/time/time-check.log"]
        env:
        - name: TIME_FREQ
          valueFrom:
            configMapKeyRef:
              name: time-config
              key: TIME_FREQ
        volumeMounts:
        - mountPath: /opt/finance/time
          name: log-volume
      volumes:
      - name: log-volume
        emptyDir: {}
    ```

    Save and close the file. Then, create the Pod:

    ```bash
    kubectl create -f pod.yaml
    ```

    This step creates a Pod named `time-check` in the `datacenter` namespace. The Pod uses the `busybox:latest` image and runs a loop that logs the date every 12 seconds to a file. It mounts a volume at `/opt/finance/time` to store the log file .

3. **Verify the Pod and ConfigMap**:

    ```bash
    kubectl get pods -n datacenter
    kubectl get configmaps -n datacenter
    ```

    This step ensures that the Pod and ConfigMap are created successfully in the `datacenter` namespace.

4. **Check the logs**:

    ```bash
    kubectl exec -it time-check -n datacenter -- sh
    cd /opt/finance/time
    cat time-check.log
    ```

    This step allows you to enter the `time-check` Pod and verify that the log file is being updated as expected.

### References
- [Kubernetes ConfigMap Concepts](https://kubernetes.io/docs/concepts/configuration/configmap/)
- [Configuring a Pod to Use a ConfigMap](https://kubernetes.io/docs/tasks/configure-pod-container/configure-pod-configmap/)
- [EmptyDir Volume](https://kubernetes.io/docs/concepts/storage/volumes/#emptydir)

[[11 Resolve Pod Deployment Issue]]