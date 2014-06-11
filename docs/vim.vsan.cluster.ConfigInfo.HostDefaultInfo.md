vim.vsan.cluster.ConfigInfo.HostDefaultInfo
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


Default VSAN service configuration to be used for hosts admitted  to the cluster.<br>See <a href="vim.vsan.cluster.ConfigInfo.md#defaultConfig">defaultConfig</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| uuid | string | true | None | VSAN service cluster UUID, in the string form  "nnnnnnnn-nnnn-nnnn-nnnn-nnnnnnnnnnnn", where n are hexadecimal  digits.   When enabling the VSAN service on the cluster, this value shall  not be specified by the user; a suitable UUID will be generated  by the platform.   While the VSAN service is enabled, this is a read-only value. |
| autoClaimStorage | bool | true | None | Whether the VSAN service is configured to automatically claim local  storage on VSAN-enabled hosts in the cluster.   If omitted while enabling the VSAN service, this value will default  to <code>true</code>.   Changing this value to <code>false</code> shall not affect any  existing disk mappings in use by hosts currently participating in  the VSAN service.   Changing this value to <code>true</code> will result in local disks  being automatically claimed for use by the VSAN service, for hosts  currently participating in the VSAN service.<br>See <a href="vim.vsan.host.ConfigInfo.StorageInfo.md#diskMapping">diskMapping</a><br>See <a href="vim.vsan.host.ConfigInfo.StorageInfo.md#autoClaimStorage">autoClaimStorage</a><br> |


