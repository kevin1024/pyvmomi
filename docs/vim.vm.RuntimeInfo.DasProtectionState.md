vim.vm.RuntimeInfo.DasProtectionState
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The DasProtectionState object describes the   vSphere HA protection state of a virtual machine (VM).

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dasProtected | bool | None | None | Whether vSphere HA is protecting a virtual machine (VM). If a   VM is protected, vSphere HA will enforce any availability   features that have been enabled for this VM. For   example, if the VM is running on a host   that fails and the VM is configured to be restarted on a failure,   then vSphere HA will attempt to restart the VM on another host.   Similarly, if you enable VM/Application Health Monitoring   for this VM, vSphere HA will monitor the heartbeats of the   VM and reset the VM when needed, as dictated by the configured   policy settings. |


