vim.LocalizationManager.MessageCatalog
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Description of an available message catalog

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| moduleName | string | None | None | The module or extension that publishes this catalog.   The moduleName will be empty for the core catalogs for the  VirtualCenter server itself. |
| catalogName | string | None | None | The name of the catalog. |
| locale | string | None | None | The locale for the catalog. |
| catalogUri | string | None | None | The URI (relative to the connection URL for the VirtualCenter server  itself) from which the catalog can be downloaded.   The caller will need to augment this with a scheme and authority (host  and port) to make a complete URL. |
| lastModified | datetime | true | None | The last-modified time of the catalog file, if available |
| md5sum | string | true | None | The checksum of the catalog file, if available |
| version | string | true | None | The version of the catalog file, if available   The format is dot-separated version string, e.g. "1.2.3". |


