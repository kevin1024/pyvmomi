vim.host.KernelModuleSystem.ModuleInfo
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about a kernel module.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | int | None | None | Module ID. |
| name | string | None | None | Module name. |
| version | string | None | None | Version string. |
| filename | string | None | None | Module filename, without the path. |
| optionString | string | None | None | Option string configured to be passed to the kernel module when loaded.   Note that this is not necessarily the option string currently in use by   the kernel module. |
| loaded | bool | None | None | Is the module loaded? |
| enabled | bool | None | None | Is the module enabled? |
| useCount | int | None | None | Number of references to this module. |
| readOnlySection | [vim.host.KernelModuleSystem.ModuleInfo.SectionInfo](vim.host.KernelModuleSystem.ModuleInfo.SectionInfo.md "vim.host.KernelModuleSystem.ModuleInfo.SectionInfo") | None | None | Read-only section information. |
| writableSection | [vim.host.KernelModuleSystem.ModuleInfo.SectionInfo](vim.host.KernelModuleSystem.ModuleInfo.SectionInfo.md "vim.host.KernelModuleSystem.ModuleInfo.SectionInfo") | None | None | Writable section information. |
| textSection | [vim.host.KernelModuleSystem.ModuleInfo.SectionInfo](vim.host.KernelModuleSystem.ModuleInfo.SectionInfo.md "vim.host.KernelModuleSystem.ModuleInfo.SectionInfo") | None | None | Text section information. |
| dataSection | [vim.host.KernelModuleSystem.ModuleInfo.SectionInfo](vim.host.KernelModuleSystem.ModuleInfo.SectionInfo.md "vim.host.KernelModuleSystem.ModuleInfo.SectionInfo") | None | None | Data section information. |
| bssSection | [vim.host.KernelModuleSystem.ModuleInfo.SectionInfo](vim.host.KernelModuleSystem.ModuleInfo.SectionInfo.md "vim.host.KernelModuleSystem.ModuleInfo.SectionInfo") | None | None | BSS section information. |


