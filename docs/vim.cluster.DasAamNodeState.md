vim.cluster.DasAamNodeState
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)
### DEPRECATED



The <a href="vim.cluster.DasAamNodeState.md">ClusterDasAamNodeState</a> data object represents the state   of the HA service on an ESX host. (AAM is a component of this service.)

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Reference to the host. |
| name | string | None | None | Name of the host  (<a href="vim.HostSystem.md">HostSystem</a>.<a href="vim.ManagedEntity.md#name">name</a>). |
| configState | string | None | None | Configuration state of the HA agent on the host.  The property can be one of the following values:  <p>  configuring<br>  error<br>  unconfiguring<br>  running<br>  <p>  <code>configState</code> represents setting or resetting the HA  configuration on the host. If the configuration operation is  successful, the value of <code>configState</code> changes  to <code>running</code>. See <a href="vim.cluster.DasAamNodeState.DasState.md">ClusterDasAamNodeStateDasState</a>. |
| runtimeState | string | None | None | The runtime state of the HA agent on the node.  The property can be one of the following values:  <p>  uninitialized<br>  initialized<br>  running<br>  error<br>  agentShutdown<br>  nodeFailed  <p>  See <a href="vim.cluster.DasAamNodeState.DasState.md">ClusterDasAamNodeStateDasState</a>. |


