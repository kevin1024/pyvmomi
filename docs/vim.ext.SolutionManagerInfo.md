vim.ext.SolutionManagerInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object encapsulates the Solution Manager configuration for  this extension.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| tab | [vim.ext.SolutionManagerInfo.TabInfo](vim.ext.SolutionManagerInfo.TabInfo.md "vim.ext.SolutionManagerInfo.TabInfo") | true | None | List of tabs that must be shown in the Solution Manager for this extension.  Tabs are shown ordered by their position in this array. |
| smallIconUrl | string | true | None | URL for an icon for this extension. The icon will be shown in the Solution  Manager for this extension. The icon must be 16x16, and should be in PNG  format. |


