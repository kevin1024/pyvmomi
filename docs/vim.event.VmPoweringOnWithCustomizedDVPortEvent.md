vim.event.VmPoweringOnWithCustomizedDVPortEvent
===============================================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when a virtual machine was powering on using   DVPorts with port level configuration, which might be different   from the DVportgroup.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnic | [vim.event.VnicPortArgument](vim.event.VnicPortArgument.md "vim.event.VnicPortArgument") | None | None | The list of Virtual NIC that were using the DVports. |


