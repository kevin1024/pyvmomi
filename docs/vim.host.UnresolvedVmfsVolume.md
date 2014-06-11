vim.host.UnresolvedVmfsVolume
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Information about detected unbound, unresolved VMFS volume.    An unresolved VMFS volume is reported when one or more device    partitions of volume are detected to have copies of extents    of the volume. Such copies can be created via replication or    snapshots.    <p>   UnresolvedVmfsVolume are not mounted on the host where they    are detected. User may choose to resignature the volume in    which case a new Uuid is assigned to the volume and contents    of the VMFS volume is kept intact.      <p>   User may choose to keep the original Uuid and mount the VMFS    volume as it is on the given host. In this case, user has    choosen to mount the copy of the VMFS volume on that host with    no change to the original Uuid. This may fail with    VmfsVolumeAlreadyMounted exception if there is an existing    VMFS volume with the same Uuid mounted somewhere in the same    datacenter.    <p>   Simple diagram representing the possible operations on UnresolvedVmfsVolume    <pre>                 resignature                 forceMount   VmfsVolume <---------------  Unresolved ------------>  VmfsVolume with   forceMountedInfo              Vmfs Volume              forceMountedInfo    not set                                                  will be set    </pre><br>See <a href="vim.host.StorageSystem.md">HostStorageSystem</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| extent | [vim.host.UnresolvedVmfsExtent](vim.host.UnresolvedVmfsExtent.md "vim.host.UnresolvedVmfsExtent") | None | None | List of detected copies of VMFS extents. |
| vmfsLabel | string | None | None | The detected VMFS label name |
| vmfsUuid | string | None | None | The detected VMFS UUID |
| totalBlocks | int | None | None | Total number of blocks in this volume. |
| resolveStatus | [vim.host.UnresolvedVmfsVolume.ResolveStatus](vim.host.UnresolvedVmfsVolume.ResolveStatus.md "vim.host.UnresolvedVmfsVolume.ResolveStatus") | None | None | Information related to how the volume might be resolved. |


