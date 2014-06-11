vim.host.VsanInternalSystem.CmmdsQuery
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


All fields in the CMMDS Query spec are optional, but at least one needs  specified to make a valid query.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | true | None | CMMDS type, e.g. DOM_OBJECT, LSOM_OBJECT, POLICY, DISK etc. |
| uuid | string | true | None | UUID of the entry. |
| owner | string | true | None | UUID of the owning node. |


