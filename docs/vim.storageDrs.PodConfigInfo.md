vim.storageDrs.PodConfigInfo
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.storageDrs.PodConfigInfo.md">StorageDrsPodConfigInfo</a> data object contains pod-wide configuration information   for the storage DRS service.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | None | None | Flag indicating whether or not storage DRS is enabled. |
| ioLoadBalanceEnabled | bool | None | None | Flag indicating whether or not storage DRS takes into account storage I/O   workload when making load balancing and initial placement recommendations. |
| defaultVmBehavior | string | None | None | Specifies the pod-wide default storage DRS behavior for virtual machines.   For currently supported storage DRS behavior, see Behavior.   You can override the default behavior for a virtual machine   by using the <a href="vim.storageDrs.VmConfigInfo.md">StorageDrsVmConfigInfo</a> object. |
| loadBalanceInterval | int | true | None | Specify the interval that storage DRS runs to load balance among datastores   within a storage pod.   <p>   Unit: minute.   The valid values are from 60 (1 hour) to 43200 (30 days).   If not specified, the default value is 480 (8 hours). |
| defaultIntraVmAffinity | bool | true | None | Specifies whether or not each virtual machine in this pod should have its virtual   disks on the same datastore by default. If set to true, virtual machines will have   all their virtual disks on the same datastore. If set to false, the virtual disks   of a virtual machine may or may not be placed on the same datastore.   If not set, the default value is true.   You can override the default behavior for a virtual machine   by using the <a href="vim.storageDrs.VmConfigInfo.md">StorageDrsVmConfigInfo</a> object. |
| spaceLoadBalanceConfig | [vim.storageDrs.SpaceLoadBalanceConfig](vim.storageDrs.SpaceLoadBalanceConfig.md "vim.storageDrs.SpaceLoadBalanceConfig") | true | None | The configuration settings for load balancing storage space. |
| ioLoadBalanceConfig | [vim.storageDrs.IoLoadBalanceConfig](vim.storageDrs.IoLoadBalanceConfig.md "vim.storageDrs.IoLoadBalanceConfig") | true | None | The configuration settings for load balancing I/O workload.   This takes effect only if <a href="vim.storageDrs.PodConfigInfo.md#ioLoadBalanceEnabled">ioLoadBalanceEnabled</a> is <code>true</code>. |
| rule | [vim.cluster.RuleInfo](vim.cluster.RuleInfo.md "vim.cluster.RuleInfo") | true | None | Pod-wide rules. |
| option | [vim.option.OptionValue](vim.option.OptionValue.md "vim.option.OptionValue") | true | None | Advanced settings. |


