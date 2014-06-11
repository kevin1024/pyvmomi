vim.OpaqueNetwork
=================
inherits from [vim.Network](vim.Network.md "vim.Network")
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This interface defines an opaque network, in the sense that the detail and configuration  of the network is unknown to vShpere and is managed by a management plane outside of  vSphere. However, the identifier and name of these networks is made available to  vSphere so that host and virtual machine virtual ethernet device can connect to them.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


