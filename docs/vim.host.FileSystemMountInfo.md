vim.host.FileSystemMountInfo
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The <a href="vim.host.FileSystemMountInfo.md">HostFileSystemMountInfo</a> data object describes   a host mount point for a file system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| mountInfo | [vim.host.MountInfo](vim.host.MountInfo.md "vim.host.MountInfo") | None | None | Information about the mount point. |
| volume | [vim.host.FileSystemVolume](vim.host.FileSystemVolume.md "vim.host.FileSystemVolume") | None | None | Information about the mounted volume. |
| vStorageSupport | string | true | None | vStorage hardware acceleration support status. This property   represents the volume's capability for storage acceleration.   See <a href="vim.host.FileSystemMountInfo.VStorageSupportStatus.md">FileSystemMountInfoVStorageSupportStatus</a> for valid   values.   <p>   If the ESX Server supports hardware acceleration, the Server   can offload specific virtual machine management operations   to a storage device with the hardware acceleration feature.   With hardware assistance, the host performs storage operations   faster and consumes less CPU, memory, and storage fabric bandwidth.   <p>   For vSphere 4.0 or earlier hosts, this value will be unset. |


