vim.host.UnresolvedVmfsResolutionResult
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


When an UnresolvedVmfsVolume has been resignatured or forceMounted, we want to    return the original spec information along with newly created VMFS volume.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| spec | [vim.host.UnresolvedVmfsResolutionSpec](vim.host.UnresolvedVmfsResolutionSpec.md "vim.host.UnresolvedVmfsResolutionSpec") | None | None | The original UnresolvedVmfsResolutionSpec which user had specified |
| vmfs | [vim.host.VmfsVolume](vim.host.VmfsVolume.md "vim.host.VmfsVolume") | true | None | Newly created VmfsVolume |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | 'fault' would be set if the operation was not successful |


