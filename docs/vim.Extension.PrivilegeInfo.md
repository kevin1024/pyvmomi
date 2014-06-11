vim.Extension.PrivilegeInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type describes privileges defined by the extension.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| privID | string | None | None | The ID of the privilege.  The format should be   &quot;&lt;group name&gt;.&lt;privilege name&gt;&quot;.   The group name should be the same as the privGroupName   property.   <p>   The privilege name should follow java package naming   conventions for uniqueness. The set of characters allowed    follow the same rules as <a href="vim.Extension.md#key">key</a>. |
| privGroupName | string | None | None | Hierarchical group name. Each level of the grouping hierarchy is   separated by a "." so group names may not include a ".".   <a href="vim.AuthorizationManager.Privilege.md#privGroupName">privGroupName</a>. |


