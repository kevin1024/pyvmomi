vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortOrderPolicy
============================================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes uplink port ordering policy for a   distributed virtual port.  A uplink port can be in the active   list, the standby list, or neither.  It cannot be in both lists.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| activeUplinkPort | string | true | None | List of active uplink ports used for load balancing. |
| standbyUplinkPort | string | true | None | Standby uplink ports used for failover. |


