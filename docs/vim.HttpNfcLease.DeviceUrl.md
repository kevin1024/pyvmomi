vim.HttpNfcLease.DeviceUrl
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Provides a mapping from logical device IDs to upload/download   URLs.   <p>   For export, a single device id is returned based on the object   identifiers for the objects.  <p>   For import, two device ids are returned. One based on the object   names used in the ImportSpec, and one based on the object    identifiers for the created objects. This is immutable and would   match the id if an ExportLease is latter created.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The immutable identifier for the device. This is set for both import/export   leases. |
| importKey | string | None | None | Identifies the device based on the names in an ImportSpec. This is only   set for import leases. |
| url | string | None | None |  |
| sslThumbprint | string | None | None | SSL thumbprint for the host the URL refers to. Empty if no SSL thumbprint  is available or needed. |
| disk | bool | true | None | Optional value to specify if the attached file is a disk in  vmdk format. |
| targetId | string | true | None | Id for this target. This only used for multi-POSTing, where a single HTTP  POST is applied to multiple targets. |
| datastoreKey | string | true | None | Key for the datastore this disk is on. This is used to look up hosts  which can be used to multi-POST disk contents, in the host map of the  lease. |
| fileSize | long | true | None | Specifies the size of the file backing for this device. This property  is only set for non-disk file backings. |


