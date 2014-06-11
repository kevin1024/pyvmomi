vim.vm.PciPassthroughInfo
=========================
inherits from [vim.vm.TargetInfo](docs/vim.vm.TargetInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Description of a generic PCI device that can be attached to a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pciDevice | [vim.host.PciDevice](vim.host.PciDevice.md "vim.host.PciDevice") | None | None | Details of the PCI device, including vendor, class and    device identification information. |
| systemId | string | None | None | The ID of the system the PCI device is attached to. |


