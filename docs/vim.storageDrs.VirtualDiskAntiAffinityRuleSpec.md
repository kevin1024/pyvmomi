vim.storageDrs.VirtualDiskAntiAffinityRuleSpec
==============================================
inherits from [vim.cluster.RuleInfo](docs/vim.cluster.RuleInfo.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Pod-wide anit-affinity rule for virtual disks. The set of virtual disks should   be placed on different datastores.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskId | int | None | None | The list of virtual disks. |


