# AWS EKS Project 🚀

This repository provides a complete Infrastructure as Code (IaC) solution to bootstrap a production-ready Amazon EKS (Elastic Kubernetes Service) cluster on AWS. It includes all essential manifests and scripts to deploy, secure, and expose your Kubernetes workloads using AWS-native integrations.

## Features

- **EKS Cluster Provisioning**: Automated setup using `eksctl` and YAML configuration.
- **Namespace & Workload Management**: Example namespace, deployment, and service manifests for rapid onboarding.
- **AWS Load Balancer Controller**: Full integration with IAM policies and service accounts for ALB/ELB support.
- **Ingress with ALB**: Secure, internet-facing ingress using AWS Application Load Balancer.
- **Modular Structure**: Organized directories for cluster, ingress, IAM, and controller resources.
- **Best Practices**: Follows AWS and Kubernetes security and tagging standards.

## Project Structure

```
aws-eks-project/
├── cluster.yaml                # EKS cluster configuration
├── deployment.yaml             # Sample app deployment
├── service.yaml                # Kubernetes service manifest
├── namespace.yaml              # Namespace definition
├── ingress/                    # Ingress resources (ALB)
├── ServiceLinkedRole-LoadBalancer-Controller/ # IAM policies & setup scripts
├── sa_ingress_class_alb_controller/           # IngressClass & controller manifests
```

## Getting Started

1. **Clone the repository**
   ```bash
   git clone https://github.com/ManishLakhara197/aws-eks-project.git
   cd aws-eks-project
   ```

2. **Provision EKS Cluster**
   ```bash
   eksctl create cluster -f cluster.yaml
   ```

3. **Configure IAM & OIDC for Load Balancer Controller**
   - Create IAM policy and associate OIDC provider (see `ServiceLinkedRole-LoadBalancer-Controller/commands.txt`).

4. **Deploy Sample Workloads**
   ```bash
   kubectl apply -f namespace.yaml
   kubectl apply -f deployment.yaml
   kubectl apply -f service.yaml
   kubectl apply -f ingress/pod-info-ingress.yaml
   ```

5. **Install AWS Load Balancer Controller**
   - Follow steps in `sa_ingress_class_alb_controller/commands.txt` and apply relevant manifests.

## Why Use This Project?

- **Fast EKS Onboarding**: Get a working cluster with best practices in minutes.
- **Production-Ready Patterns**: Includes real-world ALB ingress, IAM, and namespace separation.
- **Extensible**: Easily add more workloads, policies, or controllers.

## Connect

Created by [Manish Lakhara](https://www.linkedin.com/in/manishlakhara).  
Feel free to connect or reach out for collaboration!
