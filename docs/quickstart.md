---
layout: default
title: Quick Start
parent: Home
nav_order: 2
---

```
helm repo add o12stack https://observabilitystack.org/charts
```

# Quick Start

```
helm dependency update
helm install . --namespace=monitoring
```

```
$ kubectl get pods -n monitoring
NAME                                               READY   STATUS              RESTARTS   AGE
calico-poodle-grafana-669555c74b-8dz89             0/1     Running             0          23s
calico-poodle-prometheus-server-5f7d74449b-chzxf   0/2     ContainerCreating   0          23s
```


