vim.host.FibreChannelHba
========================
inherits from [vim.host.HostBusAdapter](docs/vim.host.HostBusAdapter.md)


This data object type describes the Fibre Channel host bus adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portWorldWideName | long | None | None | The world wide port name for the adapter. |
| nodeWorldWideName | long | None | None | The world wide node name for the adapter. |
| portType | [vim.host.FibreChannelHba.PortType](vim.host.FibreChannelHba.PortType.md "vim.host.FibreChannelHba.PortType") | None | None | The type of the fiber channel port. |
| speed | long | None | None | The current operating speed of the adapter in    bits per second. |


