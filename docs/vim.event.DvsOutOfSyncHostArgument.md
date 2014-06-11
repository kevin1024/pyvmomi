vim.event.DvsOutOfSyncHostArgument
==================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The host on which the DVS configuration is different from that   of Virtual Center server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| outOfSyncHost | [vim.event.HostEventArgument](vim.event.HostEventArgument.md "vim.event.HostEventArgument") | None | None | The host. |
| configParamters | string | None | None | The DVS configuration parameters that are different between   Virtual Center server and the host. |


