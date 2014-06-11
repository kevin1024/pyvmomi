vim.event.HostVnicConnectedToCustomizedDVPortEvent
==================================================
inherits from [vim.event.HostEvent](docs/vim.event.HostEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when some host Virtual NICs were reconfigured to use   DVPorts with port level configuration, which might be different   from the DVportgroup.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnic | [vim.event.VnicPortArgument](vim.event.VnicPortArgument.md "vim.event.VnicPortArgument") | None | None | Information about the Virtual NIC that is using the DVport. |


