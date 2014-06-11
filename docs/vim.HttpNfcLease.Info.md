vim.HttpNfcLease.Info
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This class holds information about the lease, such as the entity covered by the  lease, and HTTP URLs for up/downloading file backings.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| lease | [vim.HttpNfcLease](vim.HttpNfcLease.md "vim.HttpNfcLease") | None | None | The <a href="vim.HttpNfcLease.md">HttpNfcLease</a> object this information belongs to. |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The <a href="vim.VirtualMachine.md">VirtualMachine</a> or <a href="vim.VirtualApp.md">VirtualApp</a> this  lease covers. |
| deviceUrl | [vim.HttpNfcLease.DeviceUrl](vim.HttpNfcLease.DeviceUrl.md "vim.HttpNfcLease.DeviceUrl") | true | None | The deviceUrl property contains a mapping from logical device keys  to URLs. |
| totalDiskCapacityInKB | long | None | None | Total capacity in kilobytes of all disks in all Virtual Machines  covered by this lease. This can be used to track progress when  transferring disks. |
| leaseTimeout | int | None | None | Number of seconds before the lease times out. The client extends  the lease by calling <a href="vim.HttpNfcLease.md#progress">HttpNfcLeaseProgress</a> before  the timeout has expired. |
| hostMap | [vim.HttpNfcLease.DatastoreLeaseInfo](vim.HttpNfcLease.DatastoreLeaseInfo.md "vim.HttpNfcLease.DatastoreLeaseInfo") | true | None | Map of URLs for leased hosts for a given datastore. This is used to  look up multi-POST-capable hosts for a datastore. |


