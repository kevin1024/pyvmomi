vim.vsan.host.DiskMapping
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


A <a href="vim.vsan.host.DiskMapping.md">VsanHostDiskMapping</a> is a set of one SSD <a href="vim.host.ScsiDisk.md">HostScsiDisk</a> backed  by a set of one or more non-SSD <a href="vim.host.ScsiDisk.md">HostScsiDisk</a>. The maximum  allowed <a href="vim.vsan.host.DiskMapping.md">VsanHostDiskMapping</a> for a host is 5. A maximum set  of 6 non-SSDs <a href="vim.host.ScsiDisk.md">HostScsiDisk</a> can be added to the one  SSD <a href="vim.host.ScsiDisk.md">HostScsiDisk</a>.<br>See <a href="vim.vsan.host.ConfigInfo.StorageInfo.md">VsanHostConfigInfoStorageInfo</a><br>See vim.host.VsanSystem#initializeDisks(DiskMapping[])

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ssd | [vim.host.ScsiDisk](vim.host.ScsiDisk.md "vim.host.ScsiDisk") | None | None | SSD ScsiDisk. |
| nonSsd | [vim.host.ScsiDisk](vim.host.ScsiDisk.md "vim.host.ScsiDisk") | None | None | Set of non-SSD backing ScsiDisk. |


