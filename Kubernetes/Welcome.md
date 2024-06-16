This is a comprehensive overview of the commonly used Kubernetes commands, covering various resource types. Most of these commands can be found in the upcoming test.

**So, Good Luck**  :- )

1. **Pods:**
   - **Create a Pod:** `kubectl run pod-name --image=image-name`
   - **List Pods:** `kubectl get pods`
   - **Describe Pod:** `kubectl describe pod pod-name`
   - **Delete Pod:** `kubectl delete pod pod-name`

2. **Deployments:**
   - **Create a Deployment:** `kubectl create deployment deployment-name --image=image-name`
   - **List Deployments:** `kubectl get deployments`
   - **Scale Deployment:** `kubectl scale deployment deployment-name --replicas=3`
   - **Update Deployment Image:** `kubectl set image deployment/deployment-name container-name=image-name:new-tag`
   - **Rollout Status:** `kubectl rollout status deployment/deployment-name`
   - **Rollback Deployment:** `kubectl rollout undo deployment/deployment-name`

3. **Services:**
   - **Create a Service:** `kubectl expose deployment/deployment-name --port=80 --target-port=8080 --type=LoadBalancer`
   - **List Services:** `kubectl get services`
   - **Describe Service:** `kubectl describe service service-name`

4. **ConfigMaps:**
   - **Create a ConfigMap:** `kubectl create configmap config-map-name --from-file=path/to/file`
   - **List ConfigMaps:** `kubectl get configmaps`
   - **Describe ConfigMap:** `kubectl describe configmap config-map-name`

5. **Secrets:**
   - **Create a Secret:** `kubectl create secret generic secret-name --from-literal=key=value`
   - **List Secrets:** `kubectl get secrets`
   - **Describe Secret:** `kubectl describe secret secret-name`

6. **Namespaces:**
   - **Create a Namespace:** `kubectl create namespace namespace-name`
   - **List Namespaces:** `kubectl get namespaces`
   - **Describe Namespace:** `kubectl describe namespace namespace-name`

7. **Nodes:**
   - **List Nodes:** `kubectl get nodes`
   - **Describe Node:** `kubectl describe node node-name`

8. **Logs and Exec:**
   - **View Pod Logs:** `kubectl logs pod-name`
   - **Exec into Pod:** `kubectl exec -it pod-name -- /bin/bash`

9. **Context and Configuration:**
   - **Switch Context:** `kubectl config use-context context-name`
   - **View Config:** `kubectl config view`


[[1 Deploy Pods in Kubernetes Cluster]]
[[2 Deploy Applications with Kubernetes Deployments]]
[[3 Setup Kubernetes Namespaces and PODs]]
[[4 Set Resource Limits in Kubernetes Pods]]
[[5 Execute Rolling Updates in Kubernetes]]
[[6 Revert Deployment to Previous Version in Kubernetes]]
[[7 Deploy Replica Set in Kubernetes Cluster]]
[[8 Schedule Cronjobs in Kubernetes]]
[[9 Create Countdown Job in Kubernetes]]
[[10 Set Up Time Check Pod in Kubernetes]]
[[11 Resolve Pod Deployment Issue]]
[[12 Update Deployment and Service in Kubernetes]]
[[13 Deploy Highly Available Pods with Replication Controller]]
[[14 Resolve Volume Mounts Issue in Kubernetes]]

