vim.vm.TargetInfo
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The TargetInfo specified a  value that can be used in the device backings to   connect the virtual machine to a physical (or logical) host device.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The identification of the endpoint on the host. The format of this depends   on the kind of virtual device this endpoints is used for. For example,   for a VirtualEthernetCard this would be a networkname, and for a VirtualCDROM   it would be a device name. |
| configurationTag | string | true | None | List of configurations that this device is available for. This is only filled   out if more than one configuration is requested. |


