Here is the clean, professional `README.md` template without any extra markers:

```markdown
# 🚀 Production-Grade GitOps-Driven Microservices Platform

![AWS EKS](https://img.shields.io/badge/AWS-EKS-orange?logo=amazon-aws)
![Terraform](https://img.shields.io/badge/IaC-Terraform-purple?logo=terraform)
![ArgoCD](https://img.shields.io/badge/GitOps-ArgoCD-blue?logo=argo)
![Kubernetes](https://img.shields.io/badge/Orchestration-Kubernetes-326CE5?logo=kubernetes)

## 📌 Executive Summary
An automated, highly available microservices application platform provisioned on AWS EKS using Terraform Infrastructure as Code (IaC). The platform features zero-downtime GitOps continuous delivery via ArgoCD across an 11-microservice polyglot architecture, backed by full-stack observability using Prometheus, Grafana, and the ECK Stack (Elasticsearch, Kibana, Filebeat).

---

## 🏗️ System Architecture


```

[ Ingress / AWS Gateway API ]
│
▼
[ AWS EKS Cluster ] ──► [ ArgoCD Controller ]
├── Polyglot Microservices (11 Pods)
├── ECK Stack (Elasticsearch 9.x, Kibana, Filebeat)
└── Prometheus + Grafana Observability

```

---

## 🛠️ Tech Stack

* **Cloud Infrastructure:** AWS (EKS, VPC, Private/Public Subnets, Managed Node Groups, IAM, ALB, Route 53, ACM)
* **Infrastructure as Code (IaC):** Terraform
* **Container Orchestration & GitOps:** Kubernetes, Docker, ArgoCD, Kubernetes Gateway API, HPA
* **CI/CD & Security:** Jenkins Declarative Pipelines, GitHub Actions, SonarQube Quality Gates, Trivy, Sonatype Nexus
* **Observability & SRE:** Prometheus, Grafana, Alertmanager, Blackbox Exporter, ECK Stack (Elasticsearch, Kibana, Filebeat)

---

## 🔥 Key Features

* **Automated Provisioning:** Modular Terraform code provisioning custom multi-AZ VPC networking and managed EKS worker nodes.
* **GitOps Continuous Delivery:** ArgoCD synchronization delivering automated rolling deployments upon code push.
* **Shift-Left DevSecOps:** Integrated SonarQube quality gates and Trivy container image scanning to block critical CVEs prior to deployment.
* **Full-Stack Telemetry:** ECK Operator aggregating real-time container log events alongside Prometheus metrics and synthetic endpoint latency monitoring (~20ms).
* **Dynamic Autoscaling:** Configured Kubernetes Horizontal Pod Autoscaler (HPA) using metrics-server for traffic-adaptive scaling.

---

## 🚦 Getting Started

### Prerequisites
* AWS CLI configured with administrator permissions
* `kubectl` installed
* `terraform` >= 1.5.0
* `helm` >= 3.0

### Step 1: Provision Infrastructure
```bash
git clone [https://github.com/laksh1001/Production-Grade_GitOps-Driven_Microservices-Application.git](https://github.com/laksh1001/Production-Grade_GitOps-Driven_Microservices-Application.git)
cd terraform/
terraform init
terraform plan
terraform apply --auto-approve

```

### Step 2: Configure EKS Cluster & GitOps

```bash
aws eks update-kubeconfig --region us-east-1 --name production-eks-cluster
kubectl create namespace argocd
kubectl apply -n argocd -f [https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml](https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml)

```

---

