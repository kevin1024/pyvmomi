vim.event.RecoveryEvent
=======================
inherits from [vim.event.DvsEvent](docs/vim.event.DvsEvent.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This event is generated when recovery takes place on a management vmknic

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostName | string | None | None | The host on which recovery happened |
| portKey | string | None | None | The key of the new port |
| dvsUuid | string | true | None | The uuid of the DVS |
| vnic | string | true | None | The virtual management NIC device where recovery was done |


