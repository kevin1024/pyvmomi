vim.host.PatchManager.Result
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The result of the operation. Some of the fields are only valid for  specific operations.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| version | string | None | None | The version of the scan result schema. |
| status | [vim.host.PatchManager.Status](vim.host.PatchManager.Status.md "vim.host.PatchManager.Status") | true | None | The scan results for each patch. |
| xmlResult | string | true | None | The scan results in XML format. |


