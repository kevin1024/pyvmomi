vim.host.MultipathStateInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes the state of storage paths on the host.   All storage paths on the host are enumerated in this data object.   <p>   The reason all path state information is encapsulated in this data   object is because the path may actively change.  This data object   ensures that a request to gather path state changes only needs to   fetch this data object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| path | [vim.host.MultipathStateInfo.Path](vim.host.MultipathStateInfo.Path.md "vim.host.MultipathStateInfo.Path") | true | None | List of paths on the system and their path states. |


