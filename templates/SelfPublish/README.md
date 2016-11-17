## Self-publish stack

The aim of this stack is to automate all steps needed to publish a service in Rancher load balancers and upstream in F5 BigIP LB.

The stack will provision a load balancer service and a container running the self-configuration process.

This design (BigIP on top of Rancher load balancers) was chosen due to the fact that changes occur only when a new service is added.

For all other scenario, the Rancher load balancer is re-configured automatically by Rancher itself.

## Requirements

The following entities must exists prior to stack activation:

- BigIP partition
- BigIP route domain
- BigIP virtual server

Additionally, the virtual server must have assigned a ProxyPass irule.

## Features

- Self configuration of Rancher load balancer
- Auto configuration and sync of BigIP pool definition
- Auto configuration and sync of BigIP data group list
