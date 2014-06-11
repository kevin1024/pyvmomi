vim.host.VFlashManager.VFlashResourceRunTimeInfo
================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Data object provides vFlash resource runtime usage.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| usage | long | None | None | Overall usage of vFlash resource, in bytes. |
| capacity | long | None | None | Overall capacity of vFlash resource, in bytes. |
| accessible | bool | None | None | True if all the included the VFFS volumes are accessible. False if one or   multiple included VFFS volumes are inaccessible. |
| capacityForVmCache | long | None | None | vFlash resource capacity can be allocated for VM caches |
| freeForVmCache | long | None | None | Free vFlash resource can be allocated for VM caches |


