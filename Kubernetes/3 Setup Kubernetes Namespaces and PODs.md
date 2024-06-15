
1. **Create a namespace named `dev`**:
   ```bash
   kubectl create namespace dev
   ```
   This command creates a new namespace called `dev`. Namespaces in Kubernetes are used to divide cluster resources between multiple users or applications.

   Output:
   ```
   namespace/dev created
   ```

2. **Deploy a pod named `dev-nginx-pod` using the `nginx:latest` image in the `dev` namespace**:
   ```bash
   kubectl run dev-nginx-pod -n dev --image=nginx:latest
   ```
   This command creates a new pod named `dev-nginx-pod` in the `dev` namespace using the `nginx:latest` image. The `-n dev` flag specifies the namespace.

   Output:
   ```
   pod/dev-nginx-pod created
   ```

3. **Verify the pod is running in the `dev` namespace**:
   ```bash
   kubectl get pods -n dev
   ```
   This command lists all the pods in the `dev` namespace, showing their current status.

   Example Output:
   ```
   NAME            READY   STATUS    RESTARTS   AGE
   dev-nginx-pod   1/1     Running   0          21s
   ```

4. **Describe the pod to get detailed information**:
   ```bash
   kubectl describe pods -n dev
   ```
   This command provides detailed information about the pod `dev-nginx-pod` in the `dev` namespace, including its state, IP addresses, events, and container details.

   Example Output:
   ```
   Name:             dev-nginx-pod
   Namespace:        dev
   Priority:         0
   Service Account:  default
   Node:             kodekloud-control-plane/172.17.0.2
   Start Time:       Sat, 15 Jun 2024 02:34:53 +0000
   Labels:           run=dev-nginx-pod
   Annotations:      <none>
   Status:           Running
   IP:               10.244.0.5
   IPs:
     IP:  10.244.0.5
   Containers:
     dev-nginx-pod:
       Container ID:   containerd://c155de8cdbcfe09446446eb1818e692e82dbbcb940af31367d6a0f84584aca81
       Image:          nginx:latest
       Image ID:       docker.io/library/nginx@sha256:56b388b0d79c738f4cf51bbaf184a14fab19337f4819ceb2cae7d94100262de8
       Port:           <none>
       Host Port:      <none>
       State:          Running
         Started:      Sat, 15 Jun 2024 02:35:02 +0000
       Ready:          True
       Restart Count:  0
       Environment:    <none>
       Mounts:
         /var/run/secrets/kubernetes.io/serviceaccount from kube-api-access-8jvsw (ro)
   Conditions:
     Type              Status
     Initialized       True 
     Ready             True 
     ContainersReady   True 
     PodScheduled      True 
   Volumes:
     kube-api-access-8jvsw:
       Type:                    Projected (a volume that contains injected data from multiple sources)
       TokenExpirationSeconds:  3607
       ConfigMapName:           kube-root-ca.crt
       ConfigMapOptional:       <nil>
       DownwardAPI:             true
   QoS Class:                   BestEffort
   Node-Selectors:              <none>
   Tolerations:                 node.kubernetes.io/not-ready:NoExecute op=Exists for 300s
                                node.kubernetes.io/unreachable:NoExecute op=Exists for 300s
   Events:
     Type    Reason     Age   From               Message
     ----    ------     ----  ----               -------
     Normal  Scheduled  61s   default-scheduler  Successfully assigned dev/dev-nginx-pod to kodekloud-control-plane
     Normal  Pulling    61s   kubelet            Pulling image "nginx:latest"
     Normal  Pulled     53s   kubelet            Successfully pulled image "nginx:latest" in 8.212844918s (8.212865831s including waiting)
     Normal  Created    52s   kubelet            Created container dev-nginx-pod
     Normal  Started    52s   kubelet            Started container dev-nginx-pod
   ```

This provides a comprehensive view of the pod's creation and current state, helping you understand its status and any potential issues.

[[4 Set Resource Limits in Kubernetes Pods]]