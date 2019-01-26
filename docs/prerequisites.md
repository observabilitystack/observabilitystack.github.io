---
layout: default
title: Prerequisistes
parent: Home
nav_order: 1
---

# Setting up the target system

Before installing the observability stack into a Kubernetes cluster 
(maybe even a production system), we urge you to test things in a test
environment.
{: .fs-6 .fw-300}

We'll walk you through the installation in a local [Minikube](https://kubernetes.io/docs/setup/minikube/) installation. We use
[Homebrew](https://brew.sh/) to install software on the client side.

## Software

Have `minikube` and `helm` installed on your client:

    brew cask install minikube
    brew install kubernetes-cli helm


Set up Minikube and Helm:

<div class="code-example" markdown="1">
We use the [`hyperkit`](https://github.com/kubernetes/minikube/blob/master/docs/drivers.md#hyperkit-driver) hypervisor on our Macs as this avoids hasseling with Oracle Virtual Box.
</div>
```bash
minikube start --vm-driver=hyperkit
minikube addons enable ingress
helm init
```

### Disposing

When you're done evaluating, shut everything down

    minikube stop
    minikube delete
