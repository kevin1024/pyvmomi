vim.dvs.DistributedVirtualSwitchManager.CompatibilityResult
===========================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


This is the return type for the checkCompatibility method. This object   has a host property and optionally a fault which would   be populated only if that host is not compatible with a given dvsProductSpec.   If the host is compatible then the error property would be unset.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The host for which results are annotated. The whole object will be  filtered out if the caller did not have view permissions on the  host entity. |
| error | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | This property contains the faults that makes the host not compatible  with a given DvsProductSpec. For example, a host might not be compatible  because it's an older version of ESX that doesn't support DVS. |


