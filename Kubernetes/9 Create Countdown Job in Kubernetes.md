To create the required job named `countdown-xfusion`, you can follow these steps:

1. **Create a Job YAML configuration file**:

    ```bash
    vi job.yaml
    ```

2. **Edit the YAML file** with the following content:

    ```yaml
    apiVersion: batch/v1
    kind: Job
    metadata:
      name: countdown-xfusion
    spec:
      template:
        metadata:
          name: countdown-xfusion
        spec:
          containers:
          - name: container-countdown-xfusion
            image: centos:latest
            command: ["sleep", "5"]
          restartPolicy: Never
      backoffLimit: 4
    ```

3. **Save and exit the editor**.

4. **Create the Job using the YAML file**:

    ```bash
    kubectl create -f job.yaml
    ```

5. **Verify the creation of the Job**:

    ```bash
    kubectl get jobs
    ```

6. **Check the pods to ensure the Job is running as expected**:

    ```bash
    kubectl get pods
    ```

By following these steps, you will create a Job named `countdown-xfusion` with the specified configuration.


Reference - 

https://kubernetes.io/docs/concepts/workloads/controllers/job/

[[10 Set Up Time Check Pod in Kubernetes]]