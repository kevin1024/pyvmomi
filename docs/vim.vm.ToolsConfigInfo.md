vim.vm.ToolsConfigInfo
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


ToolsConfigInfo is a data object type containing settings for the VMware Tools   software running in the guest operating system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| toolsVersion | int | true | None | Version of VMware Tools installed on the guest operating system. |
| afterPowerOn | bool | true | None | Flag to specify whether or not scripts should run   after the virtual machine powers on. |
| afterResume | bool | true | None | Flag to specify whether or not scripts should run   after the virtual machine resumes. |
| beforeGuestStandby | bool | true | None | Flag to specify whether or not scripts should run   before the virtual machine suspends. |
| beforeGuestShutdown | bool | true | None | Flag to specify whether or not scripts should run   before the virtual machine powers off. |
| beforeGuestReboot | bool | true | None | Flag to specify whether or not scripts should run   before the virtual machine reboots. |
| toolsUpgradePolicy | string | true | None | Tools upgrade policy setting for the virtual machine.<br>See <a href="vim.vm.ToolsConfigInfo.UpgradePolicy.md">UpgradePolicy</a><br> |
| pendingCustomization | string | true | None | When set, this indicates that a customization operation is pending on the VM.   The value represents the filename of the customization package on the host. |
| syncTimeWithHost | bool | true | None | Indicates whether or not the tools program will sync time with the host time. |
| lastInstallInfo | [vim.vm.ToolsConfigInfo.ToolsLastInstallInfo](vim.vm.ToolsConfigInfo.ToolsLastInstallInfo.md "vim.vm.ToolsConfigInfo.ToolsLastInstallInfo") | true | None | Information about the last tools upgrade attempt if applicable.  This information is maintained by the server and is ignored if set by the client. |


