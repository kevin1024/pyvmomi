vim.vm.ConfigInfo.OverheadInfo
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Information about virtualization overhead required to power on the  virtual machine on the registered host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| initialMemoryReservation | long | true | None | Memory overhead required for virtual machine to be powered on (in bytes). |
| initialSwapReservation | long | true | None | Disk space required for virtual machine to be powered on (in bytes).  This space is used by virtualization infrastructure to swap out  virtual machine process memory. Location of the file is specified by  sched.swap.vmxSwapDir virtual machinge advanced config option or  in case it is not specified - current virtual machine home directory  is being used. |


