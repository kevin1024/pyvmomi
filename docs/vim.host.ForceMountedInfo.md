vim.host.ForceMountedInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


When the system detects a copy of a VmfsVolume, it will not be    auto-mounted on the host and it will be detected as    'UnresolvedVmfsVolume'.    If user decides to keep the original Uuid and mount it on the host,    it will have 'forceMounted' flag and 'forceMountedInfo' set.   'ForceMountedInfo' provides additional information specific to   user-mounted VmfsVolume.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| persist | bool | None | None | Indicates if the vmfsExtent information persistent across    host reboots. |
| mounted | bool | None | None | Indicates if the volume is currently mounted on the host |


