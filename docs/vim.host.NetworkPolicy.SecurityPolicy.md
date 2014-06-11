vim.host.NetworkPolicy.SecurityPolicy
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes security policy governing ports.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| allowPromiscuous | bool | true | None | The flag to indicate whether or not all traffic is seen    on the port. |
| macChanges | bool | true | None | The flag to indicate whether or not the Media Access    Control (MAC) address can be changed. |
| forgedTransmits | bool | true | None | The flag to indicate whether or not the virtual network adapter    should be allowed to send network traffic with a different MAC    address than that of the virtual network adapter. |


