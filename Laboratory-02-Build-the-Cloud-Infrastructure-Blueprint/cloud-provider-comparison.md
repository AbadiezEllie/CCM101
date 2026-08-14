# Cloud Provider Comparison

This document compares the core infrastructure services offered by the three major public cloud providers: Amazon Web Services (AWS), Microsoft Azure, and Google Cloud Platform (GCP), based on their official documentation.

## Service Comparison Table

| Infrastructure Component | AWS | Microsoft Azure | Google Cloud Platform |
|---|---|---|---|
| Compute | EC2 (Elastic Compute Cloud) | Virtual Machines | Compute Engine |
| Storage | S3 (Simple Storage Service) | Blob Storage | Cloud Storage |
| Networking | VPC (Virtual Private Cloud) | Virtual Network (VNet) | VPC (Global Virtual Private Cloud) |
| Identity and Access Management (IAM) | AWS IAM | Microsoft Entra ID | Cloud IAM |

## Guide Questions

### 1. Which cloud provider offers the broadest range of services? Explain your answer.
AWS, without question. It launched first back in 2006 and has had the longest runway to build out its catalog, now sitting at over 240 services. It covers everything from basic compute to genuinely obscure stuff like managed satellite ground stations and quantum computing sandboxes. Nobody else is close on breadth.

### 2. Which cloud platform would you recommend for an organization that primarily uses Microsoft products?
Azure, easily. It integrates directly with Active Directory, Windows Server, and Microsoft 365, so a company already living in that ecosystem avoids a lot of unnecessary friction. Azure Arc even extends that integration to hybrid and multi-cloud setups, which makes Azure the obvious pick here rather than a close call.

### 3. Which platform is widely recognized for Artificial Intelligence (AI), Machine Learning (ML), and Kubernetes services?
Google Cloud. Kubernetes was originally built by Google, so GKE is generally considered the most mature managed Kubernetes experience available. GCP also stands out in AI/ML through tools like Vertex AI, BigQuery ML, and custom TPU hardware built specifically for machine learning workloads.

### 4. What similarities did you observe among the three cloud providers?
Underneath the different naming schemes, all three are solving the same problems: pay-as-you-go compute, scalable storage, virtual networking, and IAM for access control. They all support managed Kubernetes, operate global data center networks, and follow a shared responsibility security model, where the provider secures the underlying infrastructure and the customer is responsible for securing what they build on top of it.
