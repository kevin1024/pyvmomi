vim.vm.device.VirtualEthernetCardOption
=======================================
inherits from [vim.vm.device.VirtualDeviceOption](docs/vim.vm.device.VirtualDeviceOption.md)


This data object type contains the options for the   virtual ethernet card data object type.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| supportedOUI | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | The valid Organizational Unique Identifiers (OUIs)   supported by this virtual Ethernet card.   <table>   <dt>Supported OUIs for statically assigned MAC addresses:</dt>   <dd>"00:50:56"</dd>   </table> |
| macType | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | The supported MAC address types. |
| wakeOnLanEnabled | [vim.option.BoolOption](vim.option.BoolOption.md "vim.option.BoolOption") | None | None | Flag to indicate whether or not wake-on-LAN is settable on this device. |
| vmDirectPathGen2Supported | bool | None | None | Flag to indicate whether VMDirectPath Gen 2 is available on this device. |


