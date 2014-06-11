vim.OvfManager.OvfFile
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Represents a file that the caller has downloaded and stored somewhere appropriate.  <p>  An instance of this class is used to tell OvfManager about the choices the caller  made about a file. This information is needed when the OVF descriptor is generated  with createDescriptor.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceId | string | None | None | The ID of the device backed by this file. This ID uniquely identifies the  device within the entity hierarchy.  <p>  The caller will have received this along with the URL needed to download the  file (this is handled by another service interface). |
| path | string | None | None | The path chosen by the caller for this file. This path becomes the value of the  "href" attribute of the corresponding "File" element in the OVF descriptor.  <p>  This path must be relative to the path chosen for the OVF descriptor. This  implies that the caller must decide in advance on the path to which it will  write the OVF descriptor, once it is returned.  <p>  The folder separator must be "/" (forward slash).  <p>  The path must not begin with a slash - ie. it must not be an absolute path. |
| compressionMethod | string | true | None | The compression method the caller chose to employ for this file. |
| chunkSize | long | true | None | The chunksize chosen by the caller.  <p>  When using chunking, the caller must adhere to the method described in the OVF  specification. |
| size | long | None | None | The file size, as observed by the caller during download. |
| capacity | long | true | None | The capacity of the disk backed by this file. This should only be set if the  device backed by this file is a disk. This value will be written in the  "capacity" attribute of the corresponding "Disk" element in the OVF descriptor.  <p>  Note that the "capacity" attribute is normally set to the capacity of the  corresponding <a href="vim.vm.device.VirtualDisk.md">VirtualDisk</a>. Setting this variable  overrides the capacity from the VirtualDisk. |
| populatedSize | long | true | None | The populated size of the disk backed by this file. This should only be set if  the device backed by this file is a disk. This value will be written in the  "populatedSize" attribute of the corresponding "Disk" element in the OVF  descriptor. |


