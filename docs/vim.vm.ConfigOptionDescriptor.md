vim.vm.ConfigOptionDescriptor
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Contains the definition of a unique key that can be used to   retrieve a configOption object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | A unique key used to identify a configOption object in this   <a href="vim.EnvironmentBrowser.md">EnvironmentBrowser</a>. |
| description | string | true | None | A description of the configOption object. |
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | List of hosts to which this descriptor applies.   List of hosts is not set when descriptor is returned   from <a href="vim.Datacenter.md#queryConfigOptionDescriptor">queryDatacenterConfigOptionDescriptor</a>. |
| createSupported | bool | None | None | Indicates whether the associated set of configuration options   can be used for virtual machine creation on a given host or   cluster. |
| defaultConfigOption | bool | None | None | Indicates whether the associated set of virtual machine   configuration options is the default one for a given host or   cluster.  Latest version is marked as default unless   other version is specified via   <a href="vim.ComputeResource.ConfigInfo.md#defaultHardwareVersionKey">defaultHardwareVersionKey</a>   or <a href="vim.Datacenter.ConfigInfo.md#defaultHardwareVersionKey">defaultHardwareVersionKey</a>.    If this setting is TRUE, virtual machine creates will use the   associated set of configuration options, unless a config version is   explicitly specified in the <a href="vim.vm.ConfigSpec.md">ConfigSpec</a>. |
| runSupported | bool | None | None | Indicates whether the associated set of configuration options   can be used to power on a virtual machine on a given host or   cluster. |
| upgradeSupported | bool | None | None | Indicates whether the associated set of configuration options   can be used as a virtual hardware upgrade target. |


