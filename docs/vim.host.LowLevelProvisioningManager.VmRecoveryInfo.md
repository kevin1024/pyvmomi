vim.host.LowLevelProvisioningManager.VmRecoveryInfo
===================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


Virtual machine information that can be used for recovery, for   example, to decide whether to register a virtual machine with a   server if the virtual machine is currently unregistered. This data   object does not contain a complete virtual machine configuration,   but a subset of information available from <a href="vim.vm.ConfigInfo.md">VirtualMachineConfigInfo</a>, all of which are available via virtual machine   configuration files.   <p>   The documentation for each property in this data object describes   the property in <a href="vim.vm.ConfigInfo.md">VirtualMachineConfigInfo</a> that contains the same   information if available.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| version | string | None | None | The hardware version of this virtual machine. Same as   <a href="vim.vm.ConfigInfo.md#version">version</a>. |
| biosUUID | string | None | None | 128-bit SMBIOS UUID of this virtual machine. Same as   <a href="vim.vm.ConfigInfo.md#uuid">uuid</a>. |
| instanceUUID | string | None | None | VirtualCenter-specific 128-bit UUID of this virtual machine. Same   as <a href="vim.vm.ConfigInfo.md#instanceUuid">instanceUuid</a>. |
| ftInfo | [vim.vm.FaultToleranceConfigInfo](vim.vm.FaultToleranceConfigInfo.md "vim.vm.FaultToleranceConfigInfo") | true | None | Fault Tolerance settings for this virtual machine. Same as   <a href="vim.vm.ConfigInfo.md#ftInfo">ftInfo</a>. Unset if non FT. |


