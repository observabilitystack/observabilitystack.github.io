---
layout: default
title: Home
nav_order: 1
has_children: true
---
# o12stack.org documentation

We strive to build a free and open source observability solution 
for Kubernetes with "smaller clusters, more of them" in mind.
{: .fs-6 .fw-300}

[Demos / Proof of concepts](https://github.com/observabilitystack/demo/blob/master/README.md){: .btn .btn-purple }
[Quick start](docs/quickstart.html){: .btn }
[View on GitHub](https://github.com/observabilitystack/k8s-stack){: .btn }

* * *

The _observabilitystack_ (o12stack) strives to combine the best-in-class 
open source monitoring and observability tools in a pre-configured turn-key 
solution. Using the Kubernetes package manager [Helm](https://helm.sh/) 
you can deploy the full stack in seconds. The stack is fully configurable 
and extendble via _Helm_. Of course you can enable and disable tools for 
a perfect fit to your infrastructure.

* * *

Coming soon
{: .label .label-yellow }

_We're currently ramping up our efforts to provide a seamless experience.
Stay tuned!_
{: .text-grey-dk-000}

## Tools to be included

* __Filebeat__ (Logfile harvester)
* __Logstash__ (Logfile enrichment and routing)
* __Elasticsearch__ (Metric storage)
* __Graylog__ (Logfile visualisation)
* __Prometheus__ (Cluster and Pod metrics)
* __Grafana__ (Metric visualisation)

## License

The Observabilitystack configuration is distributed by an [MIT license](LICENSE).

## Contributing
When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change.
