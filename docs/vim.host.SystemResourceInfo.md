vim.host.SystemResourceInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The SystemResourceInfo data object describes the configuration of   a single system resource group.  System resource groups are analogous   to <a href="vim.ResourcePool.md">ResourcePool</a> objects for virtual machines; however,   their structure is fixed and groups may not be created nor destroyed,   only configured.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | ID of the system resource group. |
| config | [vim.ResourceConfigSpec](vim.ResourceConfigSpec.md "vim.ResourceConfigSpec") | true | None | Configuration of this system resource group. |
| child | [vim.host.SystemResourceInfo](vim.host.SystemResourceInfo.md "vim.host.SystemResourceInfo") | true | None | List of child resource groups. |


