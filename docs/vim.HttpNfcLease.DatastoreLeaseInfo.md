vim.HttpNfcLease.DatastoreLeaseInfo
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


For a given datastore, represented by datastoreKey, contains a list of leased  multi-POST-capable hosts connected to it.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| datastoreKey | string | None | None | Datastore key. |
| hosts | [vim.HttpNfcLease.HostInfo](vim.HttpNfcLease.HostInfo.md "vim.HttpNfcLease.HostInfo") | None | None | List of hosts connected to this datastore and covered by this lease. The  hosts in this list are multi-POST-capable, and any one of them can be used  to transfer disks on this datastore. |


