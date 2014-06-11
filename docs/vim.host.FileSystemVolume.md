vim.host.FileSystemVolume
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Detailed information about a file system.  This is a base type for derived types   that have more specific details about specific filesystem types.   <p>   Typically a FileSystem is exposed as a datatore<br>See <a href="vim.Datastore.Info.md">DatastoreInfo</a><br>See <a href="vim.host.VmfsVolume.md">HostVmfsVolume</a><br>See <a href="vim.host.NasVolume.md">HostNasVolume</a><br>See <a href="vim.host.VffsVolume.md">HostVffsVolume</a><br>See <a href="vim.host.LocalFileSystemVolume.md">HostLocalFileSystemVolume</a><br>See <a href="vim.host.VfatVolume.md">HostVfatVolume</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| type | string | None | None | Type of file system volume.   <p>   The following values are defined:   <dl>   <dt>VMFS</dt>   <dd>     VMware File System (ESX Server only).  If this is set,     the type of the file system volume is VMFS.   </dd>    <dt>NFS</dt>   <dd>     Network file system v3 and below (Linux and ESX Server only).     If this is set, the type of the file system volume is NetworkFileSystem.   </dd>    <dt>NFSV41</dt>   <dd>     Network file system version v4.1 or later (Linux only and ESX Server only).     If this is set, the type of the file system volume is NetworkFileSystem41.   </dd>    <dt>CIFS</dt>   <dd>      Common Internet file system (Windows only). If this is set,      the type of the file system volume is CIFS.   </dd>    <dt>VFAT</dt>   <dd>      Virtual FAT (ESX Server  only). If this is set,      the type of the file system volume is VFAT.   </dd>    <dt>vsan</dt>   <dd>      VSAN (ESX Server  only). If this is set, the type of the file system      volume is VSAN.   </dd>   </dl>    <dt>VFFS</dt>   <dd>      vFlash File System (ESX Server only). If this is set, the type      of the file system volume is VFFS.   </dd>   </dl> |
| name | string | None | None | Name of the file system volume. |
| capacity | long | None | None | The capacity of the file system volume, in bytes. |


