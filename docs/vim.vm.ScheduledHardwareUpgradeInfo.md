vim.vm.ScheduledHardwareUpgradeInfo
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Data object type containing settings for the scheduled hardware upgrades.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| upgradePolicy | string | true | None | Scheduled hardware upgrade policy setting for the virtual machine.<br>See <a href="vim.vm.ScheduledHardwareUpgradeInfo.HardwareUpgradePolicy.md">ScheduledHardwareUpgradeInfoHardwareUpgradePolicy</a><br> |
| versionKey | string | true | None | Key for target hardware version to be used on next scheduled upgrade   in the format of <a href="vim.vm.ConfigOptionDescriptor.md#key">key</a>. |
| scheduledHardwareUpgradeStatus | string | true | None | Status for last attempt to run scheduled hardware upgrade.<br>See <a href="vim.vm.ScheduledHardwareUpgradeInfo.HardwareUpgradeStatus.md">ScheduledHardwareUpgradeInfoHardwareUpgradeStatus</a><br> |
| fault | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | Contains information about the failure of last attempt to run   scheduled hardware upgrade. |


