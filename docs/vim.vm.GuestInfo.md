vim.vm.GuestInfo
================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about the guest operating system.   <p>   Most of this information is collected by VMware Tools.   In general, be sure you have VMware Tools installed   and that the virtual machine is running when you access this information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| toolsStatus | [vim.vm.GuestInfo.ToolsStatus](vim.vm.GuestInfo.ToolsStatus.md "vim.vm.GuestInfo.ToolsStatus") | true | None | Current status of VMware Tools in the guest operating system, if known. |
| toolsVersionStatus | string | true | None | Current version status of VMware Tools in the guest operating system,   if known. The set of possible values is described in   <a href="vim.vm.GuestInfo.ToolsVersionStatus.md">VirtualMachineToolsVersionStatus</a> for vSphere API 5.0. |
| toolsVersionStatus2 | string | true | None | Current version status of VMware Tools in the guest operating system,   if known. The set of possible values is described in   <a href="vim.vm.GuestInfo.ToolsVersionStatus.md">VirtualMachineToolsVersionStatus</a> |
| toolsRunningStatus | string | true | None | Current running status of VMware Tools in the guest operating system,   if known. The set of possible values is described in   <a href="vim.vm.GuestInfo.ToolsRunningStatus.md">VirtualMachineToolsRunningStatus</a> |
| toolsVersion | string | true | None | Current version of VMware Tools, if known. |
| guestId | string | true | None | Guest operating system identifier (short name), if known. |
| guestFamily | string | true | None | Guest operating system family, if known. |
| guestFullName | string | true | None | Guest operating system full name, if known. |
| hostName | string | true | None | Hostname of the guest operating system, if known. |
| ipAddress | string | true | None | Primary IP address assigned to the guest operating system, if known. |
| net | [vim.vm.GuestInfo.NicInfo](vim.vm.GuestInfo.NicInfo.md "vim.vm.GuestInfo.NicInfo") | true | None | Guest information about network adapters, if known. |
| ipStack | [vim.vm.GuestInfo.StackInfo](vim.vm.GuestInfo.StackInfo.md "vim.vm.GuestInfo.StackInfo") | true | None | Guest information about IP networking stack, if known. |
| disk | [vim.vm.GuestInfo.DiskInfo](vim.vm.GuestInfo.DiskInfo.md "vim.vm.GuestInfo.DiskInfo") | true | None | Guest information about disks.  <p>  You can obtain Linux guest disk information for the following file system  types only: Ext2, Ext3, Ext4, ReiserFS, ZFS, NTFS, VFAT, UFS, PCFS, HFS, and MS-DOS. |
| screen | [vim.vm.GuestInfo.ScreenInfo](vim.vm.GuestInfo.ScreenInfo.md "vim.vm.GuestInfo.ScreenInfo") | true | None | Guest screen resolution info, if known. |
| guestState | string | None | None | Operation mode of guest operating system. One of:   <ul>    <li> "running" - Guest is running normally.    <li> "shuttingdown" - Guest has a pending shutdown command.    <li> "resetting" - Guest has a pending reset command.    <li> "standby" - Guest has a pending standby command.    <li> "notrunning" - Guest is not running.    <li> "unknown" - Guest information is not available.   </ul> |
| appHeartbeatStatus | string | true | None | Application heartbeat status.  Please see <a href="vim.VirtualMachine.AppHeartbeatStatusType.md">VirtualMachineAppHeartbeatStatusType</a> |
| appState | string | true | None | Application state.   If vSphere HA is enabled and the vm is configured for Application Monitoring  and this field's value is "appStateNeedReset" then HA will attempt immediately reset  the vm.   There are some system conditions which may delay the immediate reset. The immediate  reset will be performed as soon as allowed by vSphere HA and ESX. If during these  conditions the value is changed to appStateOk the reset will be cancelled.<br>See <a href="vim.vm.GuestInfo.AppStateType.md">GuestInfoAppStateType</a><br> |
| guestOperationsReady | bool | true | None | Guest Operations availability.   If true, the vitrual machine is ready to process guest operations. |
| interactiveGuestOperationsReady | bool | true | None | Interactive Guest Operations availability.   If true, the vitrual machine is ready to process guest operations  as the user interacting with the guest desktop. |
| generationInfo | [vim.vm.GuestInfo.NamespaceGenerationInfo](vim.vm.GuestInfo.NamespaceGenerationInfo.md "vim.vm.GuestInfo.NamespaceGenerationInfo") | true | VirtualMachine.Namespace.EventNotify | A list of namespaces and their corresponding generation numbers.  Only namespaces with non-zero  <a href="vim.vm.NamespaceManager.CreateSpec.md#maxSizeEventsFromGuest">maxSizeEventsFromGuest</a>  are guaranteed to be present here.  Use <a href="vim.vm.NamespaceManager.md#listNamespaces">ListNamespaces</a> to retrieve list of  namespaces. |


