vim.vm.Summary.GuestSummary
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A subset of virtual machine guest information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| guestId | string | true | None | Guest operating system identifier (short name), if known. |
| guestFullName | string | true | None | Guest operating system name configured on the virtual machine. |
| toolsStatus | [vim.vm.GuestInfo.ToolsStatus](vim.vm.GuestInfo.ToolsStatus.md "vim.vm.GuestInfo.ToolsStatus") | true | None | Current status of VMware Tools in the guest operating system, if known. |
| toolsVersionStatus | string | true | None | Current version status of VMware Tools in the guest operating system,   if known. |
| toolsVersionStatus2 | string | true | None | Current version status of VMware Tools in the guest operating system,   if known. |
| toolsRunningStatus | string | true | None | Current running status of VMware Tools in the guest operating system,   if known. |
| hostName | string | true | None | Hostname of the guest operating system, if known. |
| ipAddress | string | true | None | Primary IP address assigned to the guest operating system, if known. |


