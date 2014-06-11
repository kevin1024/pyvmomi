vim.vm.device.HostDiskMappingInfo
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The HostDiskMappingInfo data object type describes   a virtual disk mapping to a host disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| physicalPartition | [vim.vm.device.HostDiskMappingInfo.PartitionInfo](vim.vm.device.HostDiskMappingInfo.PartitionInfo.md "vim.vm.device.HostDiskMappingInfo.PartitionInfo") | true | None | The partition used on the host, if not mapping   to a full disk device. |
| name | string | None | None | Host resource name. |
| exclusive | bool | true | None | Flag to indicate whether or not the virtual machine has exclusive access   to the host device. |


