vim.storageDrs.PodConfigSpec
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.storageDrs.PodConfigSpec.md">StorageDrsPodConfigSpec</a> data object provides a set of update   specifications for pod-wide storage DRS configuration. To support   incremental changes, these properties are all optional.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Flag indicating whether or not storage DRS is enabled. |
| ioLoadBalanceEnabled | bool | true | None | Flag indicating whether or not storage DRS takes into account storage I/O   workload when making load balancing and initial placement recommendations. |
| defaultVmBehavior | string | true | None | Specifies the pod-wide default storage DRS behavior for virtual machines.   For currently supported storage DRS behavior, see <a href="vim.storageDrs.PodConfigInfo.Behavior.md">StorageDrsPodConfigInfoBehavior</a>.   You can override the default behavior for a virtual machine   by using the <a href="vim.storageDrs.VmConfigInfo.md">StorageDrsVmConfigInfo</a> object. |
| loadBalanceInterval | int | true | None | Specify the interval that storage DRS runs to load balance among datastores   within a storage pod. |
| defaultIntraVmAffinity | bool | true | None | Specifies whether or not each virtual machine in this pod should have its virtual   disks on the same datastore by default. |
| spaceLoadBalanceConfig | [vim.storageDrs.SpaceLoadBalanceConfig](vim.storageDrs.SpaceLoadBalanceConfig.md "vim.storageDrs.SpaceLoadBalanceConfig") | true | None | The configuration settings for load balancing storage space. |
| ioLoadBalanceConfig | [vim.storageDrs.IoLoadBalanceConfig](vim.storageDrs.IoLoadBalanceConfig.md "vim.storageDrs.IoLoadBalanceConfig") | true | None | The configuration settings for load balancing I/O workload.   This takes effect only if <a href="vim.storageDrs.PodConfigInfo.md#ioLoadBalanceEnabled">ioLoadBalanceEnabled</a> is <code>true</code>. |
| rule | [vim.cluster.RuleSpec](vim.cluster.RuleSpec.md "vim.cluster.RuleSpec") | true | None | Changes to the set of rules. |
| option | [vim.storageDrs.OptionSpec](vim.storageDrs.OptionSpec.md "vim.storageDrs.OptionSpec") | true | None | Changes to advance settings. |


