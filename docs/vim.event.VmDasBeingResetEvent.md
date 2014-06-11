vim.event.VmDasBeingResetEvent
==============================
inherits from [vim.event.VmEvent](docs/vim.event.VmEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when a virtual machine is reset by  HA VM Health Monitoring on hosts that do not support the  create screenshot api or if the createscreenshot api fails.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| reason | string | true | None | The reason why this vm is being reset |


