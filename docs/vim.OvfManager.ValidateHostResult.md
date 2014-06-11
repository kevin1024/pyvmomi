vim.OvfManager.ValidateHostResult
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| downloadSize | long | true | None | The total amount of data that must be transferred to download the entity.  <p>  This may be inaccurate due to disk compression etc. |
| flatDeploymentSize | long | true | None | The total amount of space required to deploy the entity if using flat disks. |
| sparseDeploymentSize | long | true | None | The total amount of space required to deploy the entity using sparse disks,  if known. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Errors that happened during validation. The presence of faults in this list  indicates that the validation failed. |
| warning | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Non-fatal warnings from the validation. |
| supportedDiskProvisioning | string | true | None | An array of the disk provisioning type supported by the target host system. |


