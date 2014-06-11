vim.vm.device.VirtualPCNet32Option
==================================
inherits from [vim.vm.device.VirtualEthernetCardOption](docs/vim.vm.device.VirtualEthernetCardOption.md)


The VirtualPCNet32Option data object type defines the options for the   VirtualPCNet32 data object type.  Except for the boolean    supportsMorphing option, the options are inherited from the   <a href="vim.vm.device.VirtualEthernetCardOption.md">VirtualEthernetCardOption</a> data    object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| supportsMorphing | bool | None | None | Indicates that this Ethernet card supports morphing into vmxnet when   appropriate.  This means that, if supportsMorphing="true", the virtual   AMD Lance PCNet32 Ethernet card becomes a vmxnet Ethernet card   with its added performance capabilities when appropriate. |


