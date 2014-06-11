vim.host.DiagnosticSystem
=========================


The DiagnosticSystem managed object is used to configure the diagnostic   mechanisms specific to the host.  The DiagnosticSystem interface supports   the following concepts:   <ul>     <li> Notion of an active diagnostic partition that is selected from          a set of available partitions.     <li> Ability to create a diagnostic partition that gets added to the          list of available partitions and could be made active.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='activePartition'>activePartition</a> | [vim.host.DiagnosticPartition](vim.host.DiagnosticPartition.md "vim.host.DiagnosticPartition") | true | None | The currently active diagnostic partition. |


QueryAvailablePartition()
-------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | QueryAvailablePartition |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | on some internal failure while setting the           active partition. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |




SelectActivePartition([partition](vim.host.ScsiDisk.Partition.md "vim.host.ScsiDisk.Partition"))
------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | SelectActivePartition |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the diagnostic partition does not exist. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | on some internal failure while selecting the           active partition. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the partition is not a diagnostic partition. |




QueryPartitionCreateOptions([storageType](#string "string"), [diagnosticType](#string "string"))
------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | QueryPartitionCreateOptions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | on some internal failure while querying the           create options. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid storage type is specified. |




QueryPartitionCreateDesc([diskUuid](#string "string"), [diagnosticType](#string "string"))
------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryPartitionCreateDesc |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the specified disk cannot be found.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | on some internal failure while trying to           query information about the disk.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid storage type is specified or the           specified disk is unable to accommodate a new diagnostic           partition.<br>See <a href="vim.host.ScsiDisk.md">HostScsiDisk</a><br>See <a href="vim.host.ScsiLun.md#uuid">uuid</a><br> |




CreateDiagnosticPartition([spec](vim.host.DiagnosticPartition.CreateSpec.md "vim.host.DiagnosticPartition.CreateSpec"))
-----------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | CreateDiagnosticPartition |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the specified disk cannot be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | on some internal failure while trying to           create the diagnostic partition or to activate the diagnostic           partition. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid storage type is specified or the           specified disk is unable to accommodate a new diagnostic           partition. |




