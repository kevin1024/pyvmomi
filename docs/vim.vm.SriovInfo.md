vim.vm.SriovInfo
================
inherits from [vim.vm.PciPassthroughInfo](docs/vim.vm.PciPassthroughInfo.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Description of a SRIOV device that can be attached to a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| virtualFunction | bool | None | None | Indicates whether corresponding PCI device is a virtual function   instantiated by a SR-IOV capable device. |
| pnic | string | true | None | The name of the physical nic that is represented by a SR-IOV   capable physical function. |


