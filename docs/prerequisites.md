---
layout: default
title: Prerequisistes
parent: Home
nav_order: 1
---

# Setting up the target system

We'll walk you through the installation in a local [Minikube](https://kubernetes.io/docs/setup/minikube/) installation. Adapt
these steps to install the _o12stack_ into your cluster. We use
[Homebrew](https://brew.sh/) to install software on the client side.
{: .fs-6 .fw-300}

* * *

Heads up!
{: .label .label-red }
> _Before installing the observability stack into a Kubernetes cluster 
> (maybe even a production system), we urge you to test things in a test
> environment!_

## Client

Have `minikube` and `helm` installed on your client:

    brew cask install minikube
    brew install kubernetes-cli helm

## Kubernetes cluster

Set up Minikube on your local machine. We use the [`hyperkit`](https://github.com/kubernetes/minikube/blob/master/docs/drivers.md#hyperkit-driver)
hypervisor on our Macs as this avoids hasseling with Oracle Virtual Box. The full
_o12stack_ will consume more than default memory (1GB) and cpu (1). Please provide
more memory and cpu:

```bash
minikube start --vm-driver=hyperkit --memory 8192 --cpus 3
minikube addons enable ingress
```

Set up the Helm server component _Tiller_. Check that it's up and running:
```
$ helm init
$ kubectl get pods --all-namespaces
NAMESPACE     NAME                                       READY   STATUS    RESTARTS   AGE
kube-system   tiller-deploy-69ffbf64bc-n9lss             0/1     Running   0          11s
```

## Configure ingress domain

Configure an ingress domain (or sobdomain) to point at your cluster. If you're running
Minikube, utilize `local.o12stack.org`:

```
sudo bash -c 'echo "$(minikube ip)    local.o12stack.org" >> /etc/hosts'
```

Now your good to go, [deploy the _o12stack_](quickstart.html).

### Disposing

When you're done evaluating, shut everything down and dispose the cluster.

    minikube stop
    minikube delete
