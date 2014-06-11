vim.storageDrs.VmConfigInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Storage DRS configuration for a single virtual machine. This makes it possible   to override the default behavior for an individual virtual machine.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | Reference to the virtual machine. Can be NULL during initial placement. |
| enabled | bool | true | None | Flag to indicate whether or not VirtualCenter is allowed to perform any   storage migration or initial placement recommendations for this virtual   machine on the pod <a href="vim.StoragePod.md">StoragePod</a>.   If this flag is false, the virtual machine is effectively excluded from   storage DRS.   <p>   If no individual DRS specification exists for a virtual machine,   this property defaults to true. |
| behavior | string | true | None | Specifies the particular storage DRS behavior for this virtual machine.    For supported values, see <a href="vim.storageDrs.PodConfigInfo.Behavior.md">StorageDrsPodConfigInfoBehavior</a>. |
| intraVmAffinity | bool | true | None | Specifies whether or not to have the affinity rule for the virtual disks   of this virtual machine. If not set, the default value is derived from   the pod-wide default <a href="vim.storageDrs.PodConfigInfo.md#defaultIntraVmAffinity">defaultIntraVmAffinity</a>. |
| intraVmAntiAffinity | [vim.storageDrs.VirtualDiskAntiAffinityRuleSpec](vim.storageDrs.VirtualDiskAntiAffinityRuleSpec.md "vim.storageDrs.VirtualDiskAntiAffinityRuleSpec") | true | None | Specifies the disks for this virtual machine that should be placed   on different datastores. A VM cannot have both an affinity and an   anti-affinity rule at the same time. Virtual machine disks that are   not in this rule are unconstrained and can be placed either on the   same datastore or on a different datastore as other disks from this virtual machine. |


