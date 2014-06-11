vim.host.MaintenanceSpec
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The <a href="vim.host.MaintenanceSpec.md">HostMaintenanceSpec</a> data object may be used to specify  actions to be taken by a host upon entering maintenance mode.   If the <a href="vim.host.MaintenanceSpec.md">HostMaintenanceSpec</a> or any of its fields are omitted in a  call to <a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a>, default actions  will be chosen as documented for each field's type.<br>See <a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a><br>See <a href="vim.vsan.host.DecommissionMode.md">VsanHostDecommissionMode</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vsanMode | [vim.vsan.host.DecommissionMode](vim.vsan.host.DecommissionMode.md "vim.vsan.host.DecommissionMode") | true | None | The <a href="vim.vsan.host.DecommissionMode.md">VsanHostDecommissionMode</a> for this MaintenanceSpec. |


