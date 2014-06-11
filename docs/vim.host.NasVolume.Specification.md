vim.host.NasVolume.Specification
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Specification for creating NAS volume.  <p>  When mounting a NAS volume on multiple hosts, the same remoteHost and remotePath  values should be used on every host, otherwise it will be treated as different  datastores.  For example, if one host references the remotePath of a NAS volume  as "/mnt/mount1" and another references it as "/mnt/mount1/", it will not be  recognized as the same datastore.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| remoteHost | string | None | None | The host that runs the NFS v3 or CIFS server. For NFS v4.1   and beyond use remoteHostNames defined later. The field remotehost   may be deprecated in future for NFS, so clients should plan to use the   property remoteHostNames to send in the host name(s) for both NFS v3   and v4.1 |
| remotePath | string | None | None | The remote path of the NFS mount point. |
| localPath | string | None | None | The localPath refers to the name of the NAS datastore to be created   using this specification.   <p>   In the case of ESX Server, the datastore name is a component in the   file system path at which the NAS volume can be found. For example,   if localPath is set to "nas_volume" the created NAS datastore will be   named "nas_volume" and it can be accessed via the file system path   "/vmfs/volumes/nas_volume".   <p>   In the case of VMware Server, the localPath will also be used as the   datastore name, but the datastore name may not necessarily be   reflected in the file system path where the NAS volume may be   accessed. |
| accessMode | string | None | None | Access mode for the mount point.   <p>   Mounting in read-write mode would be successful irregardless on   how the mount point is exported or access permissions. For   example, mounting a volume that is exported as read-only as   readWrite will succeed. Hence, that a readWrite mount succeeds   should not be taken as an indication that all files on a mount   is writable.   <p>   If a file system is mounted readOnly, the system cannot create   or modify any files on the file system. This is mostly useful   for storing ISO images and templates, since a virtual machine   cannot be powered on from a readOnly volume.   <p>   The access mode of a mounted NFS volume can be obtained at   <a href="vim.host.MountInfo.md#accessMode">accessMode</a>.   <p><br>See <a href="vim.host.MountInfo.AccessMode.md">HostMountMode</a><br> |
| type | string | true | None | The type of the the NAS volume (CIFS / NFS). If not specified,   defaults to nfs. |
| userName | string | true | None | If type is CIFS, the user name to use when connecting to the   CIFS server. If type is NFS, this field will be ignored. |
| password | string | true | None | If type is CIFS, the password to use when connecting to the   CIFS server. If type is NFS, this field will be ignored. |


