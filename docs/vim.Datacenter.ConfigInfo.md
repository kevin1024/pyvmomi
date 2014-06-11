vim.Datacenter.ConfigInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Configuration of the datacenter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| defaultHardwareVersionKey | string | true | None | Key for Default Hardware Version used on this datacenter   in the format of <a href="vim.vm.ConfigOptionDescriptor.md#key">key</a>.    This field affects   <a href="vim.vm.ConfigOptionDescriptor.md#defaultConfigOption">defaultConfigOption</a> returned   by <a href="vim.ComputeResource.md#environmentBrowser">environmentBrowser</a> of all its children   with this field unset. |


