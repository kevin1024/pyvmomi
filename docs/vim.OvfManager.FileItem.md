vim.OvfManager.FileItem
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


An FileItem represents a file that must be uploaded by the caller when the  inventory objects has been created in VI. These objects are created by <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a>.  <p>  Files can either be new files, in which case the "create" flag will be true, or  updates to existing files in VI. The latter is used to support the OVF parentRef  mechanism for Disks.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| deviceId | string | None | None | Uniquely identifies the device (disk, CD-ROM etc.) within the entity hierarchy.  <p>  When <a href="vim.ResourcePool.md#importVApp">ResourcePool.importVApp</a> is  called to create the <a href="vim.VirtualMachine.md">VirtualMachine</a>s and <a href="vim.VirtualApp.md">VirtualApp</a>s, it returns a map,  device ID -> URL, of where to upload the backing files. |
| path | string | None | None | The path of the item to upload, relative to the path of the OVF descriptor. |
| compressionMethod | string | true | None | The compression method as specified by the OVF  specification (for example "gzip" or "bzip2"). |
| chunkSize | long | true | None | The chunksize as specified by the OVF specification.   If this attribute is set, the "path" attribute is a prefix to  each chunk of the complete file.   For example, if chunksize is 2000000000 bytes, the actual files  might be:   myfile.000000000  (2000000000 bytes)  myfile.000000001  (2000000000 bytes)  myfile.000000002  (1500000000 bytes) |
| size | long | true | None | The complete size of the file, if it is specified in the  OVF descriptor. |
| cimType | int | None | None | The CIM type of the device for which this file provides  backing.  <p>  For example, the value 17 means "Disk drive". |
| create | bool | None | None | True if the item is not expected to exist in the infrastructure  and should therefore be created by the caller (for example using HTTP PUT). |


