vim.OvfManager.DeploymentOption
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A deployment option as defined in the OVF specfication.  <p>  This corresponds to the Configuration element of the DeploymentOptionSection in the  specification.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The key of the deployment option, corresponding to the ovf:id attribute in the  OVF descriptor |
| label | string | None | None | A localized label for the deployment option |
| description | string | None | None | A localizable description for the deployment option. |


