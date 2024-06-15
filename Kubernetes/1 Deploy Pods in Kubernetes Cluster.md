
This note provides a step-by-step explanation of the commands used to create a Kubernetes pod named `pod-nginx` using the nginx image with the latest tag.

1. **Dry-run to generate YAML configuration:**
   ```bash
   kubectl run pod-nginx --image=nginx:latest --dry-run=client -o yaml
   ```
   - `kubectl run pod-nginx`: Create a pod named `pod-nginx`.
   - `--image=nginx:latest`: Use the nginx image with the latest tag.
   - `--dry-run=client`: Simulate the command without actually creating the pod.
   - `-o yaml`: Output the configuration in YAML format.

2. **Save the YAML configuration to a file:**
   ```bash
   kubectl run pod-nginx --image=nginx:latest --dry-run=client -o yaml > pod.yaml
   ```
   - The output from the dry-run command is redirected to `pod.yaml`.

3. **Edit the YAML file to include the required labels and container name:**
   ```bash
   vi pod.yaml
   ```
   - Open `pod.yaml` in the `vi` editor.

4. **YAML configuration (`pod.yaml`):**
   ```yaml
   apiVersion: v1
   kind: Pod
   metadata:
     creationTimestamp: null
     labels:
       app: nginx_app
     name: pod-nginx
   spec:
     containers:
     - image: nginx:latest
       name: nginx-container
       resources: {}
     dnsPolicy: ClusterFirst
     restartPolicy: Always
   status: {}
   ```
   - `apiVersion: v1`: API version.
   - `kind: Pod`: Specifies that this is a pod.
   - `metadata`: Contains metadata about the pod.
     - `labels`: Add the label `app: nginx_app`.
     - `name`: Name the pod `pod-nginx`.
   - `spec`: Defines the desired state of the pod.
     - `containers`: List of containers in the pod.
       - `image`: Use the nginx image with the latest tag.
       - `name`: Name the container `nginx-container`.
   - `dnsPolicy` and `restartPolicy` are set to default values.

5. **Create the pod using the modified YAML file:**
   ```bash
   kubectl create -f pod.yaml
   ```
   - `kubectl create -f pod.yaml`: Create the pod using the configuration specified in `pod.yaml`.

6. **Verify the pod creation:**
   ```bash
   kubectl get pods
   ```
   - `kubectl get pods`: List all pods to verify that `pod-nginx` is running.

7. **Describe the pod to get detailed information:**
   ```bash
   kubectl describe pod pod-nginx
   ```
   - `kubectl describe pod pod-nginx`: Display detailed information about `pod-nginx`.

This sequence of commands ensures that a Kubernetes pod named `pod-nginx` is created with the specified configuration, including the nginx image with the latest tag, the `app` label set to `nginx_app`, and the container named `nginx-container`.


[[2 Deploy Applications with Kubernetes Deployments]]