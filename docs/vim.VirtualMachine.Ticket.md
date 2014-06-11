vim.VirtualMachine.Ticket
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This data object contains the information needed to establish a   connection to a running virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ticket | string | None | None | The ticket name. This is used as the username and password for the MKS   connection. |
| cfgFile | string | None | None | The name of the configuration file for the virtual machine. |
| host | string | true | None | The host with which to establish a connection. If the host is not specified,   it is assumed that the requesting entity knows the appropriate host with which   to connect. |
| port | int | true | None | The port number to use. If the port is not specified,  it is assumed that the requesting entity knows the appropriate port to  use when making a new connection. |
| sslThumbprint | string | true | None | The expected thumbprint of the SSL cert of the host to which  we are connecting. |


