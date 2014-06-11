vim.ResourceConfigSpec
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type is a specification for a set of resources   allocated to a virtual machine or a resource pool.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | Reference to the entity with this resource specification:   either a VirtualMachine or a ResourcePool. |
| changeVersion | string | true | None | The changeVersion is a unique identifier for a given version    of the configuration. Each change to the configuration will    update this value. This is typically implemented as an ever    increasing count or a time-stamp. However, a client should    always treat this as an opaque string.    <p>    If specified when updating the resource config., the    changes will only be applied if the current changeVersion matches the    specified changeVersion. This field can be used to guard against updates that    has happened between the configInfo was read and until it is applied. |
| lastModified | datetime | true | None | Timestamp when the resources were last modified. This is ignored when   the object is used to update a configuration. |
| cpuAllocation | [vim.ResourceAllocationInfo](vim.ResourceAllocationInfo.md "vim.ResourceAllocationInfo") | None | None | Resource allocation for CPU. |
| memoryAllocation | [vim.ResourceAllocationInfo](vim.ResourceAllocationInfo.md "vim.ResourceAllocationInfo") | None | None | Resource allocation for memory. |


