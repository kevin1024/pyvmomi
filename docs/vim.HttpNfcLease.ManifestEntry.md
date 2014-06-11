vim.HttpNfcLease.ManifestEntry
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Provides a manifest for downloaded (exported) files and disks.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Key used to match this entry with the corresponding DeviceUrl  entry in <a href="vim.HttpNfcLease.md#info">info</a>. |
| sha1 | string | None | None | SHA-1 checksum of the data stream sent from the server. This can be used  to verify that the bytes received by the client match those sent by the  HttpNfc server. |
| size | long | None | None | Size of the downloaded file. |
| disk | bool | None | None | True if the downloaded file is a virtual disk backing. |
| capacity | long | true | None | The capacity of the disk, if the file is a virtual disk backing. |
| populatedSize | long | true | None | The populated size of the disk, if the file is a virtual disk backing. |


