To create the required CronJob named `xfusion`, you can follow these steps:

Reference :- https://kubernetes.io/docs/concepts/workloads/controllers/cron-jobs/

1. **Create a CronJob YAML configuration file**:

    ```bash
    vi cronjob.yaml
    ```

2. **Edit the YAML file** with the following content:

    ```yaml
    apiVersion: batch/v1
    kind: CronJob
    metadata:
      name: xfusion
    spec:
      schedule: "*/9 * * * *"
      jobTemplate:
        spec:
          template:
            spec:
              containers:
              - name: cron-xfusion
                image: nginx:latest
                command:
                - /bin/sh
                - -c
                - echo Welcome to xfusioncorp!
              restartPolicy: OnFailure
    ```

3. **Save and exit the editor**.

4. **Create the CronJob using the YAML file**:

    ```bash
    kubectl create -f cronjob.yaml
    ```

5. **Verify the creation of the CronJob**:

    ```bash
    kubectl get cronjob
    ```

6. **Check the pods to ensure the CronJob is running as expected**:

    ```bash
    kubectl get pods
    ```

By following these steps, you will create a CronJob named `xfusion` with the specified configuration.

[[9 Create Countdown Job in Kubernetes]]