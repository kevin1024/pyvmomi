vim.ManagedEntity
=================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


ManagedEntity is an abstract base type for all managed objects present in   the inventory tree. The base type provides common functionality for traversing the   tree structure, as well as health monitoring and other basic functions.   <p>   Most Virtual Infrastructure managed object types extend this type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='parent'>parent</a> | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | System.View | Parent of this entity.   <p>   This value is null for the root object and for   <a href="vim.VirtualMachine.md">VirtualMachine</a> objects that are part of   a <a href="vim.VirtualApp.md">VirtualApp</a>. |
| <a href='customValue'>customValue</a> | [vim.CustomFieldsManager.Value](vim.CustomFieldsManager.Value.md "vim.CustomFieldsManager.Value") | true | System.View | Custom field values. |
| <a href='overallStatus'>overallStatus</a> | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | General health of this managed entity.   The overall status of the managed entity is computed as the worst status   among its alarms and the configuration issues detected on the entity.   The status is reported as one of the following values:   <ul>   <li>red:    The entity has alarms or configuration issues with a red status.   <li>yellow: The entity does not have alarms or configuration issues with a               red status, and has at least one with a yellow status.   <li>green:  The entity does not have alarms or configuration issues with a               red or yellow status, and has at least one with a green status.   <li>gray:   All of the entity's alarms have a gray status and the               configuration status of the entity is not being monitored.   </ul>    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='configStatus'>configStatus</a> | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | The configStatus indicates whether or not the system has detected a configuration   issue involving this entity. For example, it might have detected a   duplicate IP address or MAC address, or a host in a cluster   might be out of compliance. The meanings of the configStatus values are:   <ul>   <li>red:    A problem has been detected involving the entity.   <li>yellow: A problem is about to occur or a transient condition               has occurred (For example, reconfigure fail-over policy).   <li>green:  No configuration issues have been detected.   <li>gray:   The configuration status of the entity is not being monitored.   </ul>   A green status indicates only that a problem has not been detected;   it is not a guarantee that the entity is problem-free.   <p>   The <a href="vim.ManagedEntity.md#configIssue">configIssue</a> property contains a list of the   problems that have been detected.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='configIssue'>configIssue</a> | [vim.event.Event](vim.event.Event.md "vim.event.Event") | true | None | Current configuration issues that have been detected for this entity. Typically,   these issues have already been logged as events. The entity stores these   events as long as they are still current. The   <a href="vim.ManagedEntity.md#configStatus">configStatus</a> property provides an overall status   based on these events. |
| <a href='effectiveRole'>effectiveRole</a> | int | true | System.View | Access rights the current session has to this entity. |
| <a href='permission'>permission</a> | [vim.AuthorizationManager.Permission](vim.AuthorizationManager.Permission.md "vim.AuthorizationManager.Permission") | true | None | List of permissions defined for this entity. |
| <a href='name'>name</a> | string | None | System.View | Name of this entity, unique relative to its parent.   <p>   Any / (slash), \ (backslash), character used in this   name element will be escaped. Similarly, any % (percent) character used in  this name element will be escaped, unless it is used to start an escape   sequence. A slash is escaped as %2F or %2f. A backslash is escaped as %5C or   %5c, and a percent is escaped as %25. |
| <a href='disabledMethod'>disabledMethod</a> | string | true | None | List of operations that are disabled, given the current runtime   state of the entity. For example, a power-on operation always fails if a   virtual machine is already powered on. This list can be used by clients to   enable or disable operations in a graphical user interface.   <p>   Note: This list is determined by the current runtime state of an entity,   not by its permissions.   <p>   This list may include the following operations for a HostSystem:   <ul>   <li><a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a>   <li><a href="vim.HostSystem.md#exitMaintenanceMode">ExitMaintenanceMode_Task</a>   <li><a href="vim.HostSystem.md#reboot">RebootHost_Task</a>   <li><a href="vim.HostSystem.md#shutdown">ShutdownHost_Task</a>   <li><a href="vim.HostSystem.md#reconnect">ReconnectHost_Task</a>   <li><a href="vim.HostSystem.md#disconnect">DisconnectHost_Task</a>   </ul>   <p>   This list may include the following operations for a VirtualMachine:   <ul>   <li><a href="vim.VirtualMachine.md#answer">AnswerVM</a>   <li><a href="vim.ManagedEntity.md#rename">Rename_Task</a>   <li><a href="vim.VirtualMachine.md#clone">CloneVM_Task</a>   <li><a href="vim.VirtualMachine.md#powerOff">PowerOffVM_Task</a>   <li><a href="vim.VirtualMachine.md#powerOn">PowerOnVM_Task</a>   <li><a href="vim.VirtualMachine.md#suspend">SuspendVM_Task</a>   <li><a href="vim.VirtualMachine.md#reset">ResetVM_Task</a>   <li><a href="vim.VirtualMachine.md#reconfigure">ReconfigVM_Task</a>   <li><a href="vim.VirtualMachine.md#relocate">RelocateVM_Task</a>   <li><a href="vim.VirtualMachine.md#migrate">MigrateVM_Task</a>   <li><a href="vim.VirtualMachine.md#customize">CustomizeVM_Task</a>   <li><a href="vim.VirtualMachine.md#shutdownGuest">ShutdownGuest</a>   <li><a href="vim.VirtualMachine.md#standbyGuest">StandbyGuest</a>   <li><a href="vim.VirtualMachine.md#rebootGuest">RebootGuest</a>   <li><a href="vim.VirtualMachine.md#createSnapshot">CreateSnapshot_Task</a>   <li><a href="vim.VirtualMachine.md#removeAllSnapshots">RemoveAllSnapshots_Task</a>   <li><a href="vim.VirtualMachine.md#revertToCurrentSnapshot">RevertToCurrentSnapshot_Task</a>   <li><a href="vim.VirtualMachine.md#markAsTemplate">MarkAsTemplate</a>   <li><a href="vim.VirtualMachine.md#markAsVirtualMachine">MarkAsVirtualMachine</a>   <li><a href="vim.VirtualMachine.md#resetGuestInformation">ResetGuestInformation</a>   <li><a href="vim.VirtualMachine.md#mountToolsInstaller">MountToolsInstaller</a>   <li><a href="vim.VirtualMachine.md#unmountToolsInstaller">UnmountToolsInstaller</a>   <li><a href="vim.ManagedEntity.md#destroy">Destroy_Task</a>   <li><a href="vim.VirtualMachine.md#upgradeVirtualHardware">UpgradeVM_Task</a>   <li><a href="vim.VirtualMachine.md#exportVm">ExportVm</a>   </ul>   <p>   This list may include the following operations for a ResourcePool:   <ul>   <li><a href="vim.ResourcePool.md#importVApp">ImportVApp</a>   <li><a href="vim.ResourcePool.md#createVm">CreateChildVM_Task</a>   <li><a href="vim.ResourcePool.md#updateConfig">UpdateConfig</a>   <li><a href="vim.Folder.md#createVm">CreateVM_Task</a>   <li><a href="vim.ManagedEntity.md#destroy">Destroy_Task</a>   <li><a href="vim.ManagedEntity.md#rename">Rename_Task</a>   </ul>   This list may include the following operations for a VirtualApp:   <ul>   <li><a href="vim.ManagedEntity.md#destroy">Destroy_Task</a>   <li><a href="vim.VirtualApp.md#clone">CloneVApp_Task</a>   <li><a href="vim.VirtualApp.md#unregister">unregisterVApp_Task</a>   <li><a href="vim.VirtualApp.md#exportVApp">ExportVApp</a>   <li><a href="vim.VirtualApp.md#powerOn">PowerOnVApp_Task</a>   <li><a href="vim.VirtualApp.md#powerOff">PowerOffVApp_Task</a>   <li><a href="vim.VirtualApp.md#updateVAppConfig">UpdateVAppConfig</a>   </ul>  <p>    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='recentTask'>recentTask</a> | [vim.Task](vim.Task.md "vim.Task") | true | None | The set of recent tasks operating on this managed entity. This is a subset   of <a href="vim.TaskManager.md#recentTask">recentTask</a> belong to this entity. A task in this   list could be in one of the four states: pending, running, success or error.   <p>   This property can be used to deduce intermediate power states for   a virtual machine entity. For example, if the current powerState is "poweredOn"   and there is a running task performing the "suspend" operation, then the virtual   machine's intermediate state might be described as "suspending."   <p>   Most tasks (such as power operations) obtain exclusive access to the virtual   machine, so it is unusual for this list to contain more than one running task.   One exception, however, is the task of cloning a virtual machine.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='declaredAlarmState'>declaredAlarmState</a> | [vim.alarm.AlarmState](vim.alarm.AlarmState.md "vim.alarm.AlarmState") | true | System.View | A set of alarm states for alarms that apply to this managed entity.   The set includes alarms defined on this entity   and alarms inherited from the parent entity,   or from any ancestors in the inventory hierarchy.   <p>   Alarms are inherited if they can be triggered by this entity or its descendants.   This set does not include alarms that are defined on descendants of this entity. |
| <a href='triggeredAlarmState'>triggeredAlarmState</a> | [vim.alarm.AlarmState](vim.alarm.AlarmState.md "vim.alarm.AlarmState") | true | System.View | A set of alarm states for alarms triggered by this entity   or by its descendants.   <p>   Triggered alarms are propagated up the inventory hierarchy   so that a user can readily tell when a descendant has triggered an alarm.    In releases after vSphere API 5.0, vSphere Servers might not   generate property collector update notifications for this property.   To obtain the latest value of the property, you can use   PropertyCollector methods RetrievePropertiesEx or WaitForUpdatesEx.   If you use the PropertyCollector.WaitForUpdatesEx method, specify   an empty string for the version parameter. Any other version value will not   produce any property values as no updates are generated. |
| <a href='alarmActionsEnabled'>alarmActionsEnabled</a> | bool | true | System.Read | Whether alarm actions are enabled for this entity.  True if enabled; false otherwise. |
| <a href='tag'>tag</a> | [vim.Tag](vim.Tag.md "vim.Tag") | true | System.View | The set of tags associated with this managed entity.   Experimental. Subject to change. |


Reload()
--------

| service name | Reload |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




Rename([newName](#string "string"))
-----------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | Rename |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | If another object in the same folder has the target name.<br>See <a href="vim.ManagedEntity.md#name">name</a><br> |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | If the new name is not a valid entity name.<br>See <a href="vim.ManagedEntity.md#name">name</a><br> |




Destroy()
---------
 raises [vim.fault.VimFault](vim.fault.VimFault.md "vim.fault.VimFault")

---
| service name | Destroy |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | None |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.VimFault](vim.fault.VimFault.md "vim.fault.VimFault") | vim.fault.VimFault |




