vim.host.MultipathStateInfo.Path
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Data object indicating state of storage path for a named path.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Name of path.   <p>   Use this name to enable or disable storage paths <a href="vim.host.StorageSystem.md#enableMultipathPath">EnableMultipathPath</a> and <a href="vim.host.StorageSystem.md#disableMultipathPath">DisableMultipathPath</a>.   <p>   In addition to being the identifier for the path state   operations, the name is used to correlate this object to the   corresponding Path object in other contexts.<br>See <a href="vim.host.PlugStoreTopology.Path.md#name">name</a><br> |
| pathState | string | None | None | The state of the path.  Must be one of the values of    <a href="vim.host.MultipathInfo.PathState.md">MultipathState</a>. |


