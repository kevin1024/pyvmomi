vim.host.UnresolvedVmfsResolutionSpec
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


An unresolved VMFS volume is reported when one or more device partitions    of volume are detected to have copies of extents of the volume.    Such copies can be created via replication or snapshots, for example.   This data object type describes how to resolve an unbound VMFS volume.   The SCSI device path for each of the VMFS volume extent should be    specified.   For the current release, only head-extent needs to be specified.    In future releases, we will allow user to specify explicitly all the    extents which makes up a new Vmfs Volume.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| extentDevicePath | string | None | None | List of device paths each specifying a VMFS extent.   <p>   One extent must be specified.  This property is represented as a   list to enable future enhancements to the interface. |
| uuidResolution | string | None | None | When set to Resignature, new Uuid is assigned to the VMFS   volume. When set to 'forceMount', existing uuid is assigned  to the Vmfs volume and Vmfs volumes metadata doesn't change.<br>See VmfsUuidResolution |


