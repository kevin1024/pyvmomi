vim.cluster.HostPowerAction
===========================
inherits from [vim.cluster.Action](docs/vim.cluster.Action.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Describes a single host power action.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operationType | [vim.cluster.HostPowerAction.OperationType](vim.cluster.HostPowerAction.OperationType.md "vim.cluster.HostPowerAction.OperationType") | None | None | Specify whether the action is power on or power off |
| powerConsumptionWatt | int | true | None | Estimated power consumption of the host. In case of power-on,  this is the projected increase in the cluster's power  consumption. In case of power off, this is the projected  decrease in the cluster's power consumption |
| cpuCapacityMHz | int | true | None | CPU capacity of the host in units of MHz. In case of power-on  action, this is the projected increase in the cluster's CPU  capacity. In case of power off, this is the projected decrease  in the cluster's CPU capacity. |
| memCapacityMB | int | true | None | Memory capacity of the host in units of MM. In case of power-on  action, this is the projected increase in the cluster's memory  capacity. In case of power off, this is the projected decrease  in the cluster's memory capacity. |


