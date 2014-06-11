vim.HostSystem.ReconnectSpec
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Specifies the parameters needed to merge vCenter Server settings   and host settings on reconnect.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| syncState | bool | true | None | This flag should be set if on a host reconnect, state such as virtual   machine state in vCenter Server e.g. the virtual machine inventory   and autostart rules, has to be propogated to the host. Any virtual   machines that may have been unregistered or orphaned will be   reregistered according to the vCenter Server inventory. Any autostart   rules that may have changed on the host will be similarly restored.   This flag is primarily intended for stateless hosts to enable vCenter   Server to resync these hosts after a reboot. |


