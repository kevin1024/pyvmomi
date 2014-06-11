vim.host.HostBusAdapter
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the bus adapter for    the host. A host bus adapter (HBA) is a hardware   or software adapter that connects the host to storage devices.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The linkable identifier. |
| device | string | None | None | The device name of host bus adapter. |
| bus | int | None | None | The host bus number. |
| status | string | None | None | The operational status of the adapter.  Valid values include "online",   "offline", "unbound", and "unknown". |
| model | string | None | None | The model name of the host bus adapter. |
| driver | string | true | None | The name of the driver. |
| pci | string | true | None | The Peripheral Connect Interface (PCI) ID of the device    representing the host bus adapter. |


