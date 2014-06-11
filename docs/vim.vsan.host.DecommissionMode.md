vim.vsan.host.DecommissionMode
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


A <a href="vim.vsan.host.DecommissionMode.md">VsanHostDecommissionMode</a> defines an action to take upon decommissioning  a host from use with the VSAN service.   If the VSAN service DecommissionMode is omitted in a call to  <a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a>, the default action chosen  will be <a href="vim.vsan.host.DecommissionMode.ObjectAction.md#ensureObjectAccessibility">ensureObjectAccessibility</a>.<br>See <a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a><br>See <a href="vim.host.MaintenanceSpec.md#vsanMode">vsanMode</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| objectAction | string | None | None | Specifies an action to take with regard to the VSAN service upon  putting a host into maintenance mode.<br>See <a href="vim.vsan.host.DecommissionMode.ObjectAction.md">VsanHostDecommissionModeObjectAction</a><br> |


