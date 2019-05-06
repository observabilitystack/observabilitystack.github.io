---
layout: default
title: Home
nav_order: 1
has_children: true
---
# observabilitystack.org

Looking for a free open source solution to a hassle free shared nothing
observability solution in Kubernetes? Look no further, here you are.
{: .fs-6 .fw-300}

[Quick start](docs/quickstart.html){: .btn .btn-purple }
[View on GitHub](https://github.com/observabilitystack/k8s-stack){: .btn }

* * *

The _observabilitystack_ (o12stack) combines the best-in-class open source
monitoring and observability tools in a pre-configured turn-key solution.
Using the Kubernetes package manager [Helm](https://helm.sh/) you can deploy
the full stack in seconds. The stack is fully configurable and extendble 
via _Helm_. Of course you can enable and disable tools for a perfect fit 
to your infrastructure.

## Tools included

* __Prometheus__ (Cluster and Pod metrics)
* __Filebeat__ (Logfile harvester)
* __Logstash__ (Logfile enrichment and routing)
* __Elasticsearch__ (Metric storage)
* __Graylog__ (Logfile visualisation)
* __Grafana__ (Metric visualisation)

## Tools incubating

* Kibana

## License

The Observabilitystack configuration is distributed by an [MIT license](LICENSE).

## Contributing
When contributing to this repository, please first discuss the change you wish to make via issue, email, or any other method with the owners of this repository before making a change.
