vim.ExtensionManager.IpAllocationUsage
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


This data object type contains usage information about an  extension's IP allocation usage.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| extensionKey | string | None | None | Key of the extension whose usage is being  reported. |
| numAddresses | int | None | None | Number of IP addresses allocated from IP pools. |


