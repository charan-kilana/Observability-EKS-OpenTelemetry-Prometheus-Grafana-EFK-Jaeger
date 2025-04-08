## 🚀 Deploying the Application on Amazon EKS

To deploy this application on an **Amazon EKS (Elastic Kubernetes Service)** cluster, follow the steps below to create and configure the EKS cluster that will manage your nodes.

---

### ✅ Prerequisites

Ensure the following tools are installed and configured on your system:

- **kubectl** – Command-line tool for interacting with Kubernetes clusters.  
  Installation guide: [Install kubectl](https://docs.aws.amazon.com/eks/latest/userguide/install-kubectl.html)

- **eksctl** – Command-line tool to easily create and manage EKS clusters.  
  Installation guide: [Install eksctl](https://docs.aws.amazon.com/eks/latest/userguide/eksctl.html)

- **AWS CLI** – Command-line tool for working with AWS services.  
  Installation guide: [Install AWS CLI](https://docs.aws.amazon.com/cli/latest/userguide/cli-chap-install.html)

After installing the AWS CLI, configure it using the following command:

```bash
aws configure
```

## 🔍 Verifying Installed Versions

Ensure that the required tools are installed correctly.

Below is a screenshot taken from the EC2 instance showing the versions of `eksctl`, `kubectl`, and `aws` CLI:

![EKS Tool Versions](images/eks-version.png)

## 🛠️ Steps to Create EKS Cluster

### ✅ Step 1: Create an EKS Cluster

Use the following command to create an EKS cluster named `three-tier-cluster` in the `us-east-1` region:

```bash
eksctl create cluster --name three-tier-cluster --region us-east-1
```
![EKS Install](images/eks-install.png)
