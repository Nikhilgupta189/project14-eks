# Project 14: App Deployment Using Amazon EKS

## Objective
Deploy a containerized web application on Amazon Elastic Kubernetes Service (EKS) and expose it publicly using a Kubernetes LoadBalancer Service.

## Technologies Used
- Amazon EKS
- Amazon ECR
- Docker
- Kubernetes
- AWS CLI
- eksctl
- kubectl

## Implementation Steps
1. Connected to the existing EKS cluster `project14-eks`.
2. Verified the EKS cluster was ACTIVE and two worker nodes were Ready.
3. Configured Kubernetes access using `aws eks update-kubeconfig`.
4. Created a Kubernetes Deployment using `deployment.yaml`.
5. Exposed the application through a LoadBalancer Service using `service.yaml`.
6. Obtained the public AWS Load Balancer hostname.
7. Captured the required deployment and public-access screenshots.
8. Deleted the `p14-web` Deployment and Service after testing.

## Verification Commands

```bash
kubectl get nodes
kubectl get pods
kubectl get svc p14-web
```

## Screenshots

### 1. EKS Cluster Active
![EKS Cluster](screenshots/proj14_01-eks-cluster-active.png)

### 2. Kubernetes Pods and Service
![Pods and Service](screenshots/proj14_02-eks-pods-service.png)

### 3. Public Application Access
![Public Application](screenshots/proj14_03-public-app-access.png)

## Cleanup Status
The Project 14 Deployment and LoadBalancer Service were deleted successfully.

The EKS cluster remains active. A CloudFormation deletion attempt failed because resources, including an attached node group, remained. Further cleanup is pending ownership confirmation and authorization from the training administrator.

## Conclusion
The project demonstrates containerized application deployment on Amazon EKS and public exposure using Kubernetes networking.
