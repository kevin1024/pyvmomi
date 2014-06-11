vim.ComputeResource.ConfigInfo
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Configuration of the compute resource; applies to both standalone hosts   and clusters.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmSwapPlacement | string | None | None | Swapfile placement policy for virtual machines within this compute   resource. Any policy except for "inherit" is a valid value for this   property; the default is "vmDirectory". This setting will be honored   for each virtual machine within the compute resource for which the   following is true:   <ul>   <li>The virtual machine is executing on a host that has the   <a href="vim.host.Capability.md#perVmSwapFiles">perVmSwapFiles</a> capability.</li>   <li>The virtual machine configuration's   <a href="vim.vm.ConfigInfo.md#swapPlacement">swapPlacement</a> property is set   to "inherit".</li>   </ul><br>See <a href="vim.vm.ConfigInfo.SwapPlacementType.md">VirtualMachineConfigInfoSwapPlacementType</a><br> |
| spbmEnabled | bool | true | None | Flag indicating whether or not the SPBM(Storage Policy Based Management)  feature is enabled on this compute resource |
| defaultHardwareVersionKey | string | true | None | Key for Default Hardware Version used on this compute resource   in the format of <a href="vim.vm.ConfigOptionDescriptor.md#key">key</a>.    This field affects   <a href="vim.vm.ConfigOptionDescriptor.md#defaultConfigOption">defaultConfigOption</a> returned   by <a href="vim.ComputeResource.md#environmentBrowser">environmentBrowser</a> of this object and all its children   with this field unset. |


