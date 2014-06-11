vim.StorageResourceManager.IOAllocationInfo
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The IOAllocationInfo specifies the shares, limit and reservation   for storage I/O resource.   <p>   The storage I/O resource is allocated to virtual machines based on their   shares, limit and reservation. The reservation is currently exposed only   at the host level for local datastores.   And we do not support storage I/O resource management on resource pools.   <p>   Each virtual machine has one IOAllocationInfo object per virtual   disk. For example, we can specify that a virtual machine has 500 shares on   the first virtual disk, 1000 shares on the second virtual disk, etc.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| limit | long | true | None | The utilization of a virtual machine will not exceed this limit, even   if there are available resources. This is typically used to ensure a consistent   performance of virtual machines independent of available resources.   If set to -1, then there is no fixed limit on resource usage (only   bounded by available resources and shares). The unit is number of   I/O per second.   While setting the limit for storage I/O resource, if the property is unset,   it is treated as no change and the property is not updated. While reading   back the limit information of storage I/O resource, if the property is unset,   a default value of -1 will be returned, which indicates that there is no   limit on resource usage. |
| shares | [vim.SharesInfo](vim.SharesInfo.md "vim.SharesInfo") | true | None | Shares are used in case of resource contention.   The value should be within a range of 200 to 4000.   While setting shares for storage I/O resource, if the property is unset,   it is treated as no change and the property is not updated. While reading   back the shares information of storage I/O resource, if the property is unset,   a default value of <a href="vim.SharesInfo.md#level">level</a> = normal,   <a href="vim.SharesInfo.md#shares">shares</a> = 1000 will be returned. |
| reservation | int | true | None | Reservation control is used to provide guaranteed allocation in terms  of IOPS. Large IO sizes are considered as multiple IOs using a chunk  size of 32 KB as default. This control is initially supported only  at host level for local datastores. It future, it may get supported  on shared storage based on integration with Storage IO Control.  Also right now we don't do any admission control based on IO  reservation values. |


