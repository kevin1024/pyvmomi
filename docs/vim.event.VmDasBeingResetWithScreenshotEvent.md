vim.event.VmDasBeingResetWithScreenshotEvent
============================================
inherits from [vim.event.VmDasBeingResetEvent](docs/vim.event.VmDasBeingResetEvent.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This event records when a virtual machine is reset by  HA VM Health Monitoring on hosts that support the create screenshot api

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| screenshotFilePath | string | None | None | The datastore path of the screenshot taken before resetting. |


