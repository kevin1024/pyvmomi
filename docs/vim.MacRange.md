vim.MacRange
============
inherits from [vim.MacAddress](docs/vim.MacAddress.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This class defines a range of MAC address.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| address | string | None | None | MAC address. |
| mask | string | None | None | Mask that is used in matching the MAC address. A MAC address is   considered matched if the "and" operation of the mask on the   MAC address and <a href="vim.MacRange.md#address">address</a> yields the same result.   For example, a MAC of "00:A0:FF:14:FF:29" is considered matched   for a <a href="vim.MacRange.md#address">address</a> of "00:A0:C9:14:C8:29" and a   <a href="vim.MacRange.md#mask">mask</a> of "FF:FF:00:FF:00:FF". |


