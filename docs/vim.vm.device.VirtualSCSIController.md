vim.vm.device.VirtualSCSIController
===================================
inherits from [vim.vm.device.VirtualController](docs/vim.vm.device.VirtualController.md)


The VirtualSCSIController data object type represents   a SCSI controller in a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hotAddRemove | bool | true | None | All SCSI controllers support hot adding and removing of devices. This   support can't be toggled in the current implementation. Therefore, this   option is ignored when reconfiguring a SCSI controller and is always set   to "true" when reading an existing configuration. |
| sharedBus | [vim.vm.device.VirtualSCSIController.Sharing](vim.vm.device.VirtualSCSIController.Sharing.md "vim.vm.device.VirtualSCSIController.Sharing") | None | None | Mode for sharing the SCSI bus. The modes are physicalSharing,    virtualSharing, and noSharing. See the    <a href="vim.vm.device.VirtualSCSIController.Sharing.md">Sharing</a>    data object type for an explanation of these modes. |
| scsiCtlrUnitNumber | int | true | None | The unit number of the SCSI controller. The SCSI controller sits on its    own bus, so this field defines which slot the controller is using. |


