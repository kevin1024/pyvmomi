vim.DistributedVirtualSwitch.SwitchPolicy
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The switch usage policy types

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoPreInstallAllowed | bool | true | None | Whether downloading a new proxy VirtualSwitch module to the host is   allowed to be automatically executed by the switch. |
| autoUpgradeAllowed | bool | true | None | Whether upgrading of the switch is allowed to be automatically   executed by the switch. |
| partialUpgradeAllowed | bool | true | None | Whether to allow upgrading a switch when some of the hosts failed to   install the needed module. The vCenter Server will reattempt the   pre-install operation of the host module on those failed hosts,   whenever they reconnect to vCenter. |


