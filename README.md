# Kubernetes 101

This repository contains documentation and examples for practicing Kubernetes tasks based on the engineer.kodekloud.com Level 1 Kubernetes Practice. Each task is aimed at building fundamental Kubernetes skills.

## What is Kubernetes?

Kubernetes, often abbreviated as K8s, is an open-source platform designed to automate deploying, scaling, and operating application containers. Originally developed by Google, Kubernetes is now maintained by the Cloud Native Computing Foundation (CNCF). It provides a framework to run distributed systems resiliently, handling failover, scaling, and deployment seamlessly.

## What is KodeKloud?

KodeKloud is an online platform offering hands-on training for various DevOps and IT skills, including Kubernetes. It provides interactive courses and labs that simulate real-world scenarios, helping learners gain practical experience. KodeKloud's Level 1 Kubernetes Practice is designed to help beginners get up to speed with fundamental Kubernetes concepts and tasks.

## Tasks Overview

1. **Deploy Pods in Kubernetes Cluster**
    - Learn how to create and deploy Pods in a Kubernetes cluster.

2. **Deploy Applications with Kubernetes Deployments**
    - Understand Kubernetes Deployments and how to manage applications with them.

3. **Setup Kubernetes Namespaces and PODs**
    - Create and manage namespaces and deploy Pods within them.

4. **Set Resource Limits in Kubernetes Pods**
    - Configure resource requests and limits for Kubernetes Pods.

5. **Execute Rolling Updates in Kubernetes**
    - Perform rolling updates to update applications without downtime.

6. **Revert Deployment to Previous Version in Kubernetes**
    - Roll back to previous deployment versions in case of issues.

7. **Deploy Replica Set in Kubernetes Cluster**
    - Ensure high availability by deploying applications with ReplicaSets.

8. **Schedule Cronjobs in Kubernetes**
    - Automate tasks by scheduling CronJobs in Kubernetes.

9. **Create Countdown Job in Kubernetes**
    - Create and manage Jobs for specific tasks, such as countdowns.

10. **Set Up Time Check Pod in Kubernetes**
    - Deploy a Pod that performs time checks.

11. **Resolve Pod Deployment Issue**
    - Troubleshoot and fix issues in Pod deployments.

12. **Update Deployment and Service in Kubernetes**
    - Update existing Deployments and Services in a Kubernetes cluster.

13. **Deploy Highly Available Pods with Replication Controller**
    - Use ReplicationControllers to maintain high availability of Pods.

14. **Resolve Volume Mounts Issue in Kubernetes**
    - Troubleshoot and resolve volume mounting issues in Kubernetes Pods.

## Getting Started

To get started with each task, follow the detailed steps provided in the respective directories. Each task includes the necessary YAML files and commands to execute the tasks successfully.

### Prerequisites

- A working Kubernetes cluster
- `kubectl` configured to interact with the cluster

### Usage

1. Clone the repository:
    ```sh
    git clone https://github.com/dinethsiriwardana/Kubernetes-101.git
    cd Kubernetes-101
    ```

2. Navigate to the task directory you want to practice:
    ```sh
    cd task-1-deploy-pods
    ```

3. Follow the instructions in the `README.md` file within each task directory.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

## License

This project is licensed under the MIT License.

---

Happy Kubernetes practicing! 🚀
