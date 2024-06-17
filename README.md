# Kubernetes 101 [👉🏻](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/Welcome.md)

This repository contains documentation and examples for practicing Kubernetes tasks based on the [KodeKloud](https://www.kodekloud.com) Level 1 Kubernetes Practice. Each task is aimed at building fundamental Kubernetes skills.

## What is Kubernetes?

**Kubernetes**, often abbreviated as **K8s**, is an open-source platform designed to automate deploying, scaling, and operating application containers. Originally developed by Google, Kubernetes is now maintained by the [Cloud Native Computing Foundation (CNCF)](https://www.cncf.io/). It provides a framework to run distributed systems resiliently, handling failover, scaling, and deployment seamlessly.

![image](https://github.com/dinethsiriwardana/Kubernetes-101/assets/91774218/c4ad2501-0635-42af-b1f8-d8a6e4867c6b)


## What is KodeKloud?

[KodeKloud](https://www.kodekloud.com) is an online platform offering hands-on training for various DevOps and IT skills, including Kubernetes. It provides interactive courses and labs that simulate real-world scenarios, helping learners gain practical experience. KodeKloud's Level 1 Kubernetes Practice is designed to help beginners get up to speed with fundamental Kubernetes concepts and tasks.

![image](https://github.com/dinethsiriwardana/Kubernetes-101/assets/91774218/7ba92409-a519-4a72-bc0b-0abd408adb06)

<hr>

### Use [Obsidian](https://obsidian.md/) for a superior viewing experience.  <a href="https://obsidian.md/"><img src="https://github.com/dinethsiriwardana/Kubernetes-101/assets/91774218/fbd3b4a1-d261-4835-8b71-21b53c885051" alt="Obsidian Logo" width="50"></a>



## [Tasks Overview 👉🏻](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/Welcome.md)


1. **[Deploy Pods in Kubernetes Cluster](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/1%20Deploy%20Pods%20in%20Kubernetes%20Cluster.md)**
    - Learn how to create and deploy Pods in a Kubernetes cluster.

2. **[Deploy Applications with Kubernetes Deployments](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/2%20Deploy%20Applications%20with%20Kubernetes%20Deployments.md)**
    - Understand Kubernetes Deployments and how to manage applications with them.

3. **[Setup Kubernetes Namespaces and PODs](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/3%20Setup%20Kubernetes%20Namespaces%20and%20PODs.md)**
    - Create and manage namespaces and deploy Pods within them.

4. **[Set Resource Limits in Kubernetes Pods](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/4%20Set%20Resource%20Limits%20in%20Kubernetes%20Pods.md)**
    - Configure resource requests and limits for Kubernetes Pods.

5. **[Execute Rolling Updates in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/5%20Execute%20Rolling%20Updates%20in%20Kubernetes.md)**
    - Perform rolling updates to update applications without downtime.

6. **[Revert Deployment to Previous Version in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/6%20Revert%20Deployment%20to%20Previous%20Version%20in%20Kubernetes.md)**
    - Roll back to previous deployment versions in case of issues.

7. **[Deploy Replica Set in Kubernetes Cluster](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/7%20Deploy%20Replica%20Set%20in%20Kubernetes%20Cluster.md)**
    - Ensure high availability by deploying applications with ReplicaSets.

8. **[Schedule Cronjobs in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/8%20Schedule%20Cronjobs%20in%20Kubernetes.md)**
    - Automate tasks by scheduling CronJobs in Kubernetes.

9. **[Create Countdown Job in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/9%20Create%20Countdown%20Job%20in%20Kubernetes.md)**
    - Create and manage Jobs for specific tasks, such as countdowns.

10. **[Set Up Time Check Pod in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/10%20Set%20Up%20Time%20Check%20Pod%20in%20Kubernetes.md)**
    - Deploy a Pod that performs time checks.

11. **[Resolve Pod Deployment Issue](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/11%20Resolve%20Pod%20Deployment%20Issue.md)**
    - Troubleshoot and fix issues in Pod deployments.

12. **[Update Deployment and Service in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/12%20Update%20Deployment%20and%20Service%20in%20Kubernetes.md)**
    - Update existing Deployments and Services in a Kubernetes cluster.

13. **[Deploy Highly Available Pods with Replication Controller](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/13%20Deploy%20Highly%20Available%20Pods%20with%20Replication%20Controller.md)**
    - Use ReplicationControllers to maintain high availability of Pods.

14. **[Resolve Volume Mounts Issue in Kubernetes](https://github.com/dinethsiriwardana/Kubernetes-101/blob/main/Kubernetes/14%20Resolve%20Volume%20Mounts%20Issue%20in%20Kubernetes.md)**
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

This project is licensed under the [MIT License](LICENSE).

---

Happy Kubernetes practicing! 🚀
