vim.ExtendedElementDescription
==============================
inherits from [vim.ElementDescription](docs/vim.ElementDescription.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| messageCatalogKeyPrefix | string | None | None | Key to the localized message string in the catalog.  If the localized string contains parameters, values to the  parameters will be provided in #messageArg.          E.g: If the message in the catalog is   "IP address is {address}", value for "address"   will be provided by #messageArg.       Both summary and label in ElementDescription will have a corresponding  entry in the message catalog with the keys   <messageCatalogKeyPrefix>.summary and <messageCatalogKeyPrefix>.label   respectively.     ElementDescription.summary and ElementDescription.label will contain  the strings in server locale. |
| messageArg | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | Provides named arguments that can be used to localize the   message in the catalog. |


