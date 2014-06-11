vim.event.HealthStatusChangedEvent
==================================
inherits from [vim.event.Event](docs/vim.event.Event.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Event used to report change in health status of VirtualCenter components.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| componentId | string | None | None | Unique ID of the VirtualCenter component. |
| oldStatus | string | None | None | Previous health status of the component. |
| newStatus | string | None | None | Current health status of the component. |
| componentName | string | None | None | Component name. |


