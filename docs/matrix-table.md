---
hide:
  - navigation
  - toc
---

# Kubernetes Distributions & Installers Matrix Table
- [atodorov.me: Comparing Kubernetes managed services across Digital Ocean, Scaleway, OVHCloud and Linode](https://atodorov.me/2020/06/14/comparing-kubernetes-managed-services-across-digital-ocean-scaleway-ovhcloud-and-linode/)
- [Learnk8s: Comparison of Kubernetes Managed Services 🌟](https://docs.google.com/spreadsheets/d/1RPpyDOLFmcgxMCpABDzrsBYWpPYCIBuvAoUQLwOGoQw/) [Learnk8s](https://www.linkedin.com/company/learnk8s/) has compared Managed Kubernetes Services and put up online a nice sheet displaying best-breed cloud services and their Managed K8s offerings. Look for Price, Quotas, Security, etc.
- [Learnk8s: Comparison of Kubernetes Ingress controllers 🌟](https://docs.google.com/spreadsheets/d/191WWNpjJ2za6-nbG4ZoUMXMpUK8KlCIosvQB0f-oq3k/edit#gid=907731238) Daniele Polencic: "What's the best Kubernetes Ingress Controller? There is not a simple answer as some controllers are better suited for APIs, others require less maintenance, etc. To make sense of all the options, we've expanded the comparison of the Ingress controllers to include 16 Ingress controllers and several other missing features such as Hot Reloading, Proxy Protocol, Cert manager integration, etc."
- [itprotoday.com: Who's Winning in the Container Software Market 🌟](https://www.itprotoday.com/containers/whos-winning-container-software-market) Thanks to its container customer training, the $1 billion container software market is Red Hat’s to lose. Where do the other players stand?

|  Kubernetes Installer or Distribution | Role | Ecosystem | Infra Provider | On-Premise | Licence | HA | Standalone | Runs in Docker | Ingress + Storage <br/>included | Automated <br/>Deployment | Details | 
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- | 
| [kubeadm](https://github.com/kubernetes/kubeadm)| SRE / DevOps | Kubernetes Upstream | Multi platform | Yes | OSS | Yes | No | No | No | No | Official kubernetes deployment tool | 
| [Ansible role for kubeadm automation](https://github.com/geerlingguy/ansible-role-kubernetes) | SRE / DevOps | Kubernetes Upstream | Virtual Machine | Yes | OSS | Yes | Yes | No | Yes (storage?) | No | Ansible role for kubeadm automation |
| [Kops](https://github.com/kubernetes/kops)| SRE / DevOps | Kubernetes Upstream | AWS | No | OSS | Yes | No | No | Yes | Yes | AWS compliant, alpha release <br/>for other providers | 
| [kube-aws](https://kubernetes-incubator.github.io/kube-aws/)| SRE / DevOps | | | | | | | | | | A command-line tool to declaratively manage Kubernetes clusters on AWS|
| [Minikube](https://github.com/kubernetes/minikube)| Devel | Kubernetes Upstream | Dektop Virtual Machine | Yes | OSS | No | Yes | No | No | Yes | Official development environment |
| [Docker Desktop on Windows](https://docs.docker.com/docker-for-windows/#kubernetes)| Devel | Kubernetes Upstream | Desktop Virtual Machine | Yes | OSS | No | Yes | Yes | No | Yes | Development environment available in <br/>Docker Desktop on Windows | 
| [Rancher 2](https://rancher.com/docs/rancher/v2.x/en/)| SRE / DevOps | Multi-cloud kubernetes <br/>management | Virtual Machine | Yes | OSS | Yes | No | No | No | No | Racher is an enterprise kubernetes installer <br/>that competes with OpenShift. | 
| [Rancher 2 RKE](https://rancher.com/products/rke/)| SRE / DevOps | Rancher | Virtual Machine | Yes | OSS | Yes | Yes | Yes | no | no | Rancher 2 that runs in docker containers. | 
| [K3s](https://k3s.io/)| SRE / DevOps / IoT | Rancher | Virtual Machine | Yes | OSS | Yes | Yes | No | Yes | Yes | Basic kubernetes with automated installer. |
| [K3d](https://github.com/rancher/k3d)| SRE / DevOps / IoT | Rancher | Virtual Machine | Yes | OSS | Yes | Yes | Yes | Yes | Yes | k3s that runs in docker containers. | 
| [K3sup (said 'ketchup')](https://github.com/alexellis/k3sup)| SRE / DevOps / IoT | Rancher | Virtual Machine | Yes | OSS | Yes | Yes | No | Yes | Yes | get from zero to KUBECONFIG with k3s on any local or remote VM |
| [K3OS](https://github.com/rancher/k3os)| SRE / DevOps / IoT | Rancher | Virtual Machine | Yes | OSS | Yes | Yes | No | Yes | Yes | Linux distribution designed to remove as much OS maintenance as <br/>possible in a Kubernetes cluster | 
| [K3c](https://github.com/rancher/k3c)| Devel | Rancher | Linux | Yes | OSS | No | Yes | No | No | Yes | Lightweight local container engine for container development (experiment) |
| [Microk8s](https://microk8s.io/)| Devel / IoT | Kubernetes Upstream | Virtual Machine | Yes | OSS | Yes (beta) | Yes | No | Yes | Yes | Ubuntu. It compites with k3s. |
| [Pharos](https://k8spharos.dev/)| SRE / DevOPs / IoT | Kubernetes Upstream | Multi Platform | Yes | OSS | Yes | Yes | No | Yes | Yes | Pharos is a vendor neutral community driven Kubernetes that works on any infrastructure at any scale. It works flawlessly on public clouds, private clouds, hybrid clouds, on-premises, bare metal or at the edge, no problem! | 
| [OKD](https://github.com/okd-community-install)| SRE / DevOps | OpenShift | Virtual Machine | Yes | OSS | Yes | Yes | No | Yes <br/>(okd-community-install) | Yes <br/>(okd-community-install) | okd-community-install is a standalone cluster <br/>of 1 node valid for small projects. | 
| [Minishift](https://www.okd.io/minishift/)| Devel | OpenShift | Desktop Virtual Machine | Yes | OSS | No | Yes | No | No | Yes | OpenShift 3 official development environment. | 
| [OCP 4 CodeReady Containers](https://try.openshift.com)| Devel | OpenShift | Desktop Virtual Machine | Yes | OSS | No | Yes | No | No | Yes | OpenShift 4 official development environment |
| [OCP 4 Public Cloud](https://try.openshift.com)| SRE / DevOps | OpenShift | AWS, GCP, Azure | No | Yes | Yes | No | No | Yes | Yes | OpenShift in Public Cloud | 
| [OpenShift Dedicated](https://try.openshift.com) | SRE / DevOps | OpenShift | AWS | No | Yes | Yes | No | No | Yes | Yes | OpenShift In AWS managed by Red Hat | 
| [OCP 4 Private Cloud 1](https://try.openshift.com)| SRE / DevOps | OpenShift | OpenStack, <br/>Red Hat Virtualization | Yes | Yes | Yes | No | No | Yes | Yes | OpenShift in private cloud with automated <br/>deployment recommeded by Red Hat. | 
| [OCP 4 Private Cloud 2](https://try.openshift.com)| SRE / DevOps | OpenShift | vSphere 6.7 U2, Bare Metal | Yes | Yes | Yes | No | No | Yes | No | OpenShift in private cloud with infra providers <br/>that currently don't support automated <br/>deployments. |
| [AWS EKS](https://aws.amazon.com/en/eks/)| SRE / DevOps | AWS Kubernetes | AWS | No | N/A | Yes | No | No | Yes | Yes | Managed kubernetes by AWS | 
| [Azure AKS](https://azure.microsoft.com/en-en/services/kubernetes-service/)| SRE / DevOps | Azure Kubernetes | Azure | No | N/A | Yes | No | No | Yes | Yes | Managed kubernetes by Azure | 
| [Google kubernetes Engine (GKE)](https://cloud.google.com/kubernetes-engine/)| SRE / DevOps | Google Kubernetes | GCP | No | N/A | Yes | No | No | Yes | Yes | Managed kubernetes by Google Cloud | 
| [Digital Ocean Kubernetes](https://www.digitalocean.com/products/kubernetes/)| SRE / DevOps | Digital Ocean Kubernetes | Digital Ocean | No | N/A | Yes | No | No | Yes | Yes | Managed kubernetes by Digital Ocean Cloud | 
| [Alibaba Container Service for kubernetes (ACK)](https://www.alibabacloud.com/product/kubernetes) | | SRE / DevOps | Alibaba Kubernetes | Alibaba Cloud | No | N/A | Yes | No | No | yes | Yes | Managed kubernetes by Alibaba Cloud |
| [Oracle Kubernetes Engine (OKE)](https://www.oracle.com/cloud/compute/container-engine-kubernetes.html)| SRE / DevOps | Oracle Kubernetes | Oracle Cloud | No | N/A | Yes | No | No | Yes | Yes | Managed kubernetes by Oracle Cloud | 
| [Terraform (kubernetes the hard way)](https://napo.io/posts/kubernetes-the-real-hard-way-on-aws/)| SRE / DevOps | Kubernetes Upstream | AWS EKS, Google GKE, <br/>Azure AKS, Digital Ocean, <br/>Alibaba, Oracle Cloud | No | N/A | Yes | No | No | Yes | No | kubernetes installer compliant with all the major public cloud providers<br/> (the hard way). It does not use the official installers offered by each <br/>cloud provider. | 
| [Kubespray on Public Cloud](https://github.com/kubernetes-sigs/kubespray)| SRE / DevOps | Kubernetes Upstream | AWS, GCE, Azure, <br/>Oracle Cloud (experimental) | Yes | OSS | Yes | Yes | No | Yes | Yes |  | 
| [Kubespray on Private Cloud](https://github.com/kubernetes-sigs/kubespray)| SRE / DevOps | Kubernetes Upstream | OpenStack, vSphere, <br/>Packet (bare metal), or baremetal | Yes | OSS | Yes | Yes | No | Yes | No |  |
| [Conjure-up ](https://conjure-up.io/)| SRE / DevOps | Kubernetes Upstream |  | Yes | OSS | Yes | Yes | No | Yes | Yes |  | 
| [weave.works](https://www.weave.works/)| SRE / DevOps / Devel |  Kubernetes Upstream |  | | |  |  | |  |  |  |
| [WKSctl](https://github.com/weaveworks/wksctl)| SRE / DevOps | Kubernetes Upstream |  | Yes | OSS | Yes | Yes | No | Yes | Yes |  |
| [Caravan](https://engineering.linecorp.com/en/blog/building-large-kubernetes-clusters/)| SRE / DevOps | Kubernetes Upstream |  | Yes | OSS | Yes | Yes | No | Yes | Yes |  |
| [ClusterAPI](https://cluster-api.sigs.k8s.io/)| SRE / DevOps | Kubernetes Upstream |  | Yes | OSS | Yes | No | No | No |  |  | 
| [Kind](https://github.com/kubernetes-sigs/kind)| Devel | Kubernetes Upstream |  | Yes | OSS | No | Yes | Yes | No | Yes | Not designed for production use; it is intended for development and <br/>testing environments. | 
| [k0s](https://k0sproject.io/)| SRE / DevOps | | | Yes | OSS | Yes | Yes | No | Yes | Yes | Developed by Mirantis | 
| [Ubuntu Charmed Kubernetes](https://ubuntu.com/kubernetes/features)| SRE / DevOps / Devel |  Kubernetes Upstream |  | | |  |  | |  |  |  |
| [VMware Pivotal Container Service (PKS)](https://pivotal.io/platform/pivotal-container-service)| SRE / DevOps | PKS / Cloud Foundry PaaS <br/>(no kubernetes) | vSphere, multi-cloud, public-cloud | Yes | Yes | Yes | No | No | Yes | Yes | Pivotal Container Service (PKS) adquired by VMware in 2019. <br/>Cloud Foundry PaaS that compites with kubernetes. | 
| [VMware vSphere 7 with Kubernetes](https://www.vmware.com/products/vsphere.html)| SRE / DevOps | VMware Kubernetes | vSphere | Yes | Yes | Yes | No | No | Yes | Yes | VMware's kubernetes | 
| [VMware Kubernetes Tanzu (PKS renamed)](https://cloud.vmware.com/tanzu)| SRE / DevOps | VMware Kubernetes | vSphere, multi-cloud, public-cloud | Yes | Yes | Yes | No | No | Yes | Yes | Embed kubernetes natively into vSphere. Competes with OpenShift. | 
| [Mirantis Docker Enterprise 3.1+ with Kubernetes](https://www.mirantis.com/software/docker/docker-enterprise/)| SRE / DevOps | Mirantis Kubernetes | multi-cloud, private & public cloud | Yes | Yes | Yes | No | No | Yes | Yes | Istio, Windows and Linux Worker nodes| 
| [K8e](https://github.com/xiaods/k8e) |  |  |  |  |  |  |  |  |  |  | Simple Kubernetes Distribution. Builds on upstream project K3s as codebase, remove Edge/IoT features and extend enterprise features with best practices | 
| [Typhoon](https://github.com/poseidon/typhoon) |  |  |  |  |  |  |  |  |  |  | Minimal and free Kubernetes distribution with Terraform | 
|====================================|==================|======================|==========================|  |  |  |  |  |  |  |=============================================|==============================================================================|
