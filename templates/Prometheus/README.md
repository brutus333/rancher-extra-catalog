### Prometheus stack

[Prometheus](https://github.com/prometheus) is an open-source systems monitoring and alerting toolkit originally built at SoundCloud. Since its inception in 2012, many companies and organizations have adopted Prometheus, and the project has a very active developer and user community. It is now a standalone open source project and maintained independently of any company. To emphasize this and clarify the project's governance structure, Prometheus joined the Cloud Native Computing Foundation in 2016 as the second hosted project after Kubernetes.

##Features

Prometheus's main features are:

 - a multi-dimensional data model (time series identified by metric name and key/value pairs)
 - a flexible query language to leverage this dimensionality
 - no reliance on distributed storage; single server nodes are autonomous
 - time series collection happens via a pull model over HTTP
 - pushing time series is supported via an intermediary gateway
 - targets are discovered via service discovery or static configuration
 - multiple modes of graphing and dashboarding support

This Rancher stack put together several components to monitor efficiently docker containers under Rancher umbrella:
 
 - [ranch-eye](https://github.com/infinityworksltd/ranch-eye): Simple haproxy (1.6) implementation for exposing rancher's implementation of cadvisor stats to an external endpoint.
 - [prom-rancher-sd](https://github.com/brutus333/prom-rancher-sd): This utility was created to integrate prometheus monitoring to application running in Docker containers.
 - prometheus: the monitoring tool itself
 - node_exporter: Prometheus exporter for OS statistics


