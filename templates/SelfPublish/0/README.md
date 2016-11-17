## Add SelfPublish stack

SelfPublish stack for automated BigIP publishing

## Info

This catalog template deploys one load balancing service and one self-configuration service. The stack needs BigIP credentials and some configuration items for configuration changes in BigIP.

## Usage

Select SelfPublish stack from the catalog; complete all fields and deploy.

The following label should be setup on a service in the same environment as the self publishing stack in order to be published:

```
com.rancher.published=${stack_name}
```

where stack_name is the name of the self publishing stack (this was added to allow for multiple selfpublishing stacks in the same env)
