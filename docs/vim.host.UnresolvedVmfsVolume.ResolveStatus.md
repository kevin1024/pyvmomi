vim.host.UnresolvedVmfsVolume.ResolveStatus
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Data object that describes the resolvability of a volume.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| resolvable | bool | None | None | Can this volume be resolved?  There may be other reasons a volume cannot   be resolved other than the fact that it is incomplete.  This boolean will   authoritatively indicate if the server can resolve this volume. |
| incompleteExtents | bool | true | None | Is the list of extents for the volume a partial list?  A volume can only   be resignatured if all extents composing that volume are available.   Hence, a volume with a partial extent list cannot be resignatured.   <p>   In cases where this information is not known for a volume, this   property will be unset. |
| multipleCopies | bool | true | None | Are there multiple copies of extents for this volume?  If any extent of   the volume has multiple copies then the extents to be resolved must be   explicitly specified when resolving this volume.   <p>   In cases where this information is not known for a volume, this   property will be unset. |


