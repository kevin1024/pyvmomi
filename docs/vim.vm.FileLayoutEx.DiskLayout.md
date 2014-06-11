vim.vm.FileLayoutEx.DiskLayout
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Layout of a virtual disk, including the base- and delta- disks.   <p>   A virtual disk typically is made up of a chain of disk-units.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | Identifier for the virtual disk in <a href="vim.vm.VirtualHardware.md#device">device</a>. |
| chain | [vim.vm.FileLayoutEx.DiskUnit](vim.vm.FileLayoutEx.DiskUnit.md "vim.vm.FileLayoutEx.DiskUnit") | true | None | The disk-unit chain that makes up this virtual disk. |


