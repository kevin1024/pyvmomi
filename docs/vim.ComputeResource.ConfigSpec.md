vim.ComputeResource.ConfigSpec
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


Changes to apply to the compute resource configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vmSwapPlacement | string | true | None | New setting for the swapfile placement policy. Any change to this   policy will affect virtual machines that subsequently power on or   resume from a suspended state in this compute resource, or that   migrate to a host in this compute resource while powered on; virtual   machines that are currently powered on in this compute resource will   not yet be affected.<br>See <a href="vim.vm.ConfigInfo.SwapPlacementType.md">VirtualMachineConfigInfoSwapPlacementType</a><br> |
| spbmEnabled | bool | true | None | Flag indicating whether or not the SPBM(Storage Policy Based Management)  feature is enabled on this compute resource |
| defaultHardwareVersionKey | string | true | None | Key for Default Hardware Version to be used on this compute resource   in the format of <a href="vim.vm.ConfigOptionDescriptor.md#key">key</a>.    Setting this field affects   <a href="vim.vm.ConfigOptionDescriptor.md#defaultConfigOption">defaultConfigOption</a> returned   by <a href="vim.ComputeResource.md#environmentBrowser">environmentBrowser</a> of this object and all its children   with this field unset. |


