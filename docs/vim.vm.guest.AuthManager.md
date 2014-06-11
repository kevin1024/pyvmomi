vim.vm.guest.AuthManager
========================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


AuthManager is the managed object that provides APIs  to manipulate the guest operating authentication.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


ValidateCredentialsInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"))
------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault")

---
| service name | ValidateCredentialsInGuest |
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
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to support     the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported by     the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due to     guest agent configuration. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |




AcquireCredentialsInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [requestedAuth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"))
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TooManyGuestLogons](vim.fault.TooManyGuestLogons.md "vim.fault.TooManyGuestLogons"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.GuestAuthenticationChallenge](vim.fault.GuestAuthenticationChallenge.md "vim.fault.GuestAuthenticationChallenge"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault")

---
| service name | AcquireCredentialsInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestAuthenticationChallenge](vim.fault.GuestAuthenticationChallenge.md "vim.fault.GuestAuthenticationChallenge") | if the credential information     provided requires a challenge to authenticate. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to     support the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due     to guest agent configuration. |
| [vim.fault.TooManyGuestLogons](vim.fault.TooManyGuestLogons.md "vim.fault.TooManyGuestLogons") | if there are too many concurrent login     sessions active in the guest. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |




ReleaseCredentialsInGuest([vm](vim.VirtualMachine.md "vim.VirtualMachine"), [auth](vim.vm.guest.GuestAuthentication.md "vim.vm.guest.GuestAuthentication"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable"), [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState"), [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest"), [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate"), [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault")

---
| service name | ReleaseCredentialsInGuest |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.GuestOperationsFault](vim.fault.GuestOperationsFault.md "vim.fault.GuestOperationsFault") | if there is an error processing a guest     operation. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the virtual machine is busy. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the operation cannot be performed because of the      virtual machine's current state. |
| [vim.fault.GuestOperationsUnavailable](vim.fault.GuestOperationsUnavailable.md "vim.fault.GuestOperationsUnavailable") | if the VM agent for guest operations     is not running. |
| [vim.fault.InvalidPowerState](vim.fault.InvalidPowerState.md "vim.fault.InvalidPowerState") | if the VM is not powered on. |
| [vim.fault.GuestComponentsOutOfDate](vim.fault.GuestComponentsOutOfDate.md "vim.fault.GuestComponentsOutOfDate") | if the guest agent is too old to     support the operation. |
| [vim.fault.OperationNotSupportedByGuest](vim.fault.OperationNotSupportedByGuest.md "vim.fault.OperationNotSupportedByGuest") | if the operation is not supported     by the guest OS. |
| [vim.fault.OperationDisabledByGuest](vim.fault.OperationDisabledByGuest.md "vim.fault.OperationDisabledByGuest") | if the operation is not enabled due     to guest agent configuration. |
| [vim.fault.InvalidGuestLogin](vim.fault.InvalidGuestLogin.md "vim.fault.InvalidGuestLogin") | if the the guest authentication information     was not accepted. |




