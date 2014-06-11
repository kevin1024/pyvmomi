vim.dvs.VmwareDistributedVirtualSwitch.SecurityPolicy
=====================================================
inherits from [vim.InheritablePolicy](docs/vim.InheritablePolicy.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes security policy governing ports.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| allowPromiscuous | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not all traffic is seen   on the port. |
| macChanges | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not the Media Access   Control (MAC) address can be changed. |
| forgedTransmits | [vim.BoolPolicy](vim.BoolPolicy.md "vim.BoolPolicy") | true | None | The flag to indicate whether or not the virtual network adapter   should be allowed to send network traffic with a different MAC   address than that of the virtual network adapter. |


