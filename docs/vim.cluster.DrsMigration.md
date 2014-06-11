vim.cluster.DrsMigration
========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Describes a single virtual machine migration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | A unique key that identifies this recommendation. This    is used as an argument to    ComputeResource.applyRecommendation. |
| time | datetime | None | None | The time this recommendation was computed. |
| vm | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | The virtual machine selected for migration. |
| cpuLoad | int | true | None | Current CPU load for the virtual machine, in MHz.   This property is only populated for recommendations. |
| memoryLoad | long | true | None | Current memory load for the virtual machine, in bytes.   This field is only populated for recommendations. |
| source | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Source host. |
| sourceCpuLoad | int | true | None | Current CPU load on the source host, in MHz. |
| sourceMemoryLoad | long | true | None | Current memory usage on the source host, in bytes. |
| destination | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Destination host. |
| destinationCpuLoad | int | true | None | Current CPU load on the destination host, in MHz. |
| destinationMemoryLoad | long | true | None | Current memory usage on the destination host, in bytes. |


