vim.event.VmRestartedOnAlternateHostEvent
=========================================
inherits from [vim.event.VmPoweredOnEvent](docs/vim.event.VmPoweredOnEvent.md)
### DEPRECATED



This event records that the virtual machine was restarted on a host, since   its original host had failed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sourceHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The host that failed. |


