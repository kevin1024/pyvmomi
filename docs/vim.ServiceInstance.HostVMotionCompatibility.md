vim.ServiceInstance.HostVMotionCompatibility
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The object type for the array returned by queryVMotionCompatibility;   specifies the VMotion compatibility types for a host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | The prospective host for the virtual machine. |
| compatibility | string | true | None | Ways in which the host is compatible with the designated virtual   machine that is a candidate for VMotion. This array will be   a subset of the set of VMotionCompatibilityType strings that   were input to queryVMotionCompatibility. |


