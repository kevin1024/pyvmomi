vim.vm.guest.FileManager
========================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


FileManager is the managed object that provides APIs  to manipulate the guest operating system files.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


MakeDirectoryInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [directoryPath](#string "string"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | MakeDirectoryInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the directory cannot be created because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.FileAlreadyExists](vim.fault.FileAlreadyExists.md "vim.fault.FileAlreadyExists") | if the specified object already exists. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




DeleteFileInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [filePath](#string "string"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.NotAFile](vim.fault.NotAFile.md "vim.fault.NotAFile"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | DeleteFileInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.NotAFile](vim.fault.NotAFile.md "vim.fault.NotAFile") | if the specified object is not a file. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




DeleteDirectoryInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [directoryPath](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.NotADirectory](vim.fault.NotADirectory.md "vim.fault.NotADirectory"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | DeleteDirectoryInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.NotADirectory](vim.fault.NotADirectory.md "vim.fault.NotADirectory") | if the specified object is not a directory. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




MoveDirectoryInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [srcDirectoryPath](#string "string"), [dstDirectoryPath](#string "string"))
----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | MoveDirectoryInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




MoveFileInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [srcFilePath](#string "string"), [dstFilePath](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | MoveFileInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




CreateTemporaryFileInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [prefix](#string "string"), [suffix](#string "string"), [directoryPath](#string "string"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | CreateTemporaryFileInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




CreateTemporaryDirectoryInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [prefix](#string "string"), [suffix](#string "string"), [directoryPath](#string "string"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | CreateTemporaryDirectoryInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




ListFilesInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [filePath](#string "string"), [matchPattern](#string "string"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | ListFilesInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | vim.fault.FileFault |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the matchPattern is an invalid regular     expression. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |




ChangeFileAttributesInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [guestFilePath](#string "string"), [fileAttributes](vim.vm.guest.FileManager.FileAttributes.md "vim.vm.guest.FileManager.FileAttributes"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | ChangeFileAttributesInGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due     to guest agent configuration. |




InitiateFileTransferFromGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [guestFilePath](#string "string"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | InitiateFileTransferFromGuest |
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
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | If the guest agent is too old to     support the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | If the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | If the operation is not enabled due     to guest agent configuration. |




InitiateFileTransferToGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"), [guestFilePath](#string "string"), [fileAttributes](vim.vm.guest.FileManager.FileAttributes.md "vim.vm.guest.FileManager.FileAttributes"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied")

---
| service name | InitiateFileTransferToGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.FileFault](vim.fault.FileFault.md "vim.fault.FileFault") | if there is a file error in the guest operating system. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestPermissionDenied](vim.fault.GuestPermissionDenied.md "vim.fault.GuestPermissionDenied") | if the operation fails because     the guest authentication will not allow the operation. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | If the guest agent is too old to     support the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | If the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | If the operation is not enabled due to     guest agent configuration. |




