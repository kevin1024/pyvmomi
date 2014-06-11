vim.vm.guest.ProcessManager
===========================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


ProcessManager is the managed object that provides APIs  to manipulate the guest operating system processes.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


StartProgramInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [spec](vim.vm.guest.ProcessManager.ProgramSpec.md "vim.vm.guest.ProcessManager.ProgramSpec"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | StartProgramInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type | None |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the program path does not exist. |
| [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile") | if the program path cannot be accessed. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the program path cannot be run because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported by     the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




ListProcessesInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"))
------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | ListProcessesInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if there are insufficient permissions in     the guest OS. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




TerminateProcessInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"))
---------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.GuestProcessNotFound](vim.fault.GuestProcessNotFound.md "vim.fault.GuestProcessNotFound"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | TerminateProcessInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestProcessNotFound](vim.fault.GuestProcessNotFound.md "vim.fault.GuestProcessNotFound") | if the pid does not refer to a valid process. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the process cannot be terminated because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to     support the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due     to guest agent configuration. |




ReadEnvironmentVariableInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [names](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | ReadEnvironmentVariableInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy.     accepted by the guest OS. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if there are insufficient permissions in     the guest OS. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




