vim.Datacenter.ConfigSpec
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Changes to apply to the datacenter configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| defaultHardwareVersionKey | string | true | None | Key for Default Hardware Version to be used on this datacenter   in the format of <a href="vim.vm.ConfigOptionDescriptor.md#key">key</a>.    Setting this field affects   <a href="vim.vm.ConfigOptionDescriptor.md#defaultConfigOption">defaultConfigOption</a> returned   by <a href="vim.ComputeResource.md#environmentBrowser">environmentBrowser</a> of all its children   with this field unset. |


