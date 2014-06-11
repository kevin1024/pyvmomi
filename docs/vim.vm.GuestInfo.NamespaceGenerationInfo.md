vim.vm.GuestInfo.NamespaceGenerationInfo
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The namespace name as the unique key. |
| generationNo | int | None | None | Namespace generation number.  Generation number is changed whenever  there is new unread event pending from the guest to the VMODL. |


