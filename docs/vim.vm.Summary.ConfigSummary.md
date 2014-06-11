vim.vm.Summary.ConfigSummary
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A subset of virtual machine configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Name of the virtual machine. |
| template | bool | None | None | Flag to determine whether or not this virtual machine is a template. |
| vmPathName | string | None | None | Path name to the configuration file for the virtual machine |
| memorySizeMB | int | true | None | Memory size of the virtual machine, in megabytes. |
| cpuReservation | int | true | None | Configured CPU reservation in MHz |
| memoryReservation | int | true | None | Configured Memory reservation in MB |
| numCpu | int | true | None | Number of processors in the virtual machine. |
| numEthernetCards | int | true | None | Number of virtual network adapters. |
| numVirtualDisks | int | true | None | Number of virtual disks attached to the virtual machine. |
| uuid | string | true | None | Virtual machine BIOS identification. |
| instanceUuid | string | true | None | VC-specific identifier of the virtual machine |
| guestId | string | true | None | Guest operating system identifier (short name). |
| guestFullName | string | true | None | Guest operating system name configured on the virtual machine. |
| annotation | string | true | None | Description for the virtual machine. |
| product | [vim.vApp.ProductInfo](vim.vApp.ProductInfo.md "vim.vApp.ProductInfo") | true | None | Product information. References to properties in the URLs are expanded. |
| installBootRequired | bool | true | None | Whether the VM requires a reboot to finish installation. False if no vApp  meta-data is configured. |
| ftInfo | [vim.vm.FaultToleranceConfigInfo](vim.vm.FaultToleranceConfigInfo.md "vim.vm.FaultToleranceConfigInfo") | true | None | Fault Tolerance settings for this virtual machine.   This property will be populated only for fault tolerance virtual   machines and will be left unset for all other virtual machines.   See <a href="vim.vm.FaultToleranceConfigInfo.md">FaultToleranceConfigInfo</a> for a description. |
| managedBy | [vim.ext.ManagedByInfo](vim.ext.ManagedByInfo.md "vim.ext.ManagedByInfo") | true | None | Specifies that this VM is managed by a VC Extension. See the  <a href="vim.vm.ConfigSpec.md#managedBy">managedBy</a> property in the ConfigSpec  for more details. |


