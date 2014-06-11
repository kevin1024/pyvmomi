vim.Capability
==============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A particular product may or may not support certain features. This data object    indicates whether or not a service instance implements these features. This data    object type indicates the circumstances under which an operation throws a    <a href="vmodl.fault.NotSupported.md">NotSupported</a> fault.   <p>   Support for some features is indicated by the presence or absence of   the manager object from the service instance. For example, the AlarmManager manager    object indicates collecting alarms is supported.   Other features indicate whether or not a given operation on an   object throws a <a href="vmodl.fault.NotSupported.md">NotSupported</a> fault.   <p>   Some capabilities depend on the host or virtual machine   version. These are specified by using the vim.host.Capability and   vim.vm.Capability objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| provisioningSupported | bool | None | None | Indicates whether or not the service instance supports provisioning.   For example, the <a href="vim.VirtualMachine.md#clone">CloneVM</a> operation. |
| multiHostSupported | bool | None | None | Indicates whether or not the service instance supports multiple hosts. |
| userShellAccessSupported | bool | None | None | Flag indicating whether host user accounts should have the option to   be granted shell access |
| supportedEVCMode | [vim.EVCMode](vim.EVCMode.md "vim.EVCMode") | true | None | All supported Enhanced VMotion Compatibility modes. |
| networkBackupAndRestoreSupported | bool | true | None | Indicates whether network backup and restore feature is supported. |


