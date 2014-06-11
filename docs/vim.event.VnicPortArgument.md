vim.event.VnicPortArgument
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This argument records a Virtual NIC device that connects to a DVPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnic | string | None | None | The Virtual NIC devices that were using the DVports. |
| port | [vim.dvs.PortConnection](vim.dvs.PortConnection.md "vim.dvs.PortConnection") | None | None | The DVPorts that were being used. |


