vim.host.PhysicalNic
====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the physical network adapter    as seen by the primary operating system.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | true | None | The linkable identifier. |
| device | string | None | None | The device name of the physical network adapter. |
| pci | string | None | None | Device hash of the PCI device corresponding to this    physical network adapter. |
| driver | string | true | None | The name of the driver. |
| linkSpeed | [vim.host.PhysicalNic.LinkSpeedDuplex](vim.host.PhysicalNic.LinkSpeedDuplex.md "vim.host.PhysicalNic.LinkSpeedDuplex") | true | None | The current link state of the physical network adapter.     If this object is not set, then the link is down. |
| validLinkSpecification | [vim.host.PhysicalNic.LinkSpeedDuplex](vim.host.PhysicalNic.LinkSpeedDuplex.md "vim.host.PhysicalNic.LinkSpeedDuplex") | true | None | The valid combinations of speed and duplexity for this    physical network adapter.   The speed and the duplex settings usually must be configured    as a pair.  This array lists all the valid combinations available    for a physical network adapter.   <p>   Autonegotiate is not listed as one of the combinations supported.   If is implicitly supported by the physical network adapter   unless <a href="vim.host.PhysicalNic.md#autoNegotiateSupported">autoNegotiateSupported</a> is set to false. |
| spec | [vim.host.PhysicalNic.Specification](vim.host.PhysicalNic.Specification.md "vim.host.PhysicalNic.Specification") | None | None | The specification of the physical network adapter. |
| wakeOnLanSupported | bool | None | None | Flag indicating whether the NIC is wake-on-LAN capable |
| mac | string | None | None | The media access control (MAC) address of the physical   network adapter. |
| fcoeConfiguration | [vim.host.FcoeConfig](vim.host.FcoeConfig.md "vim.host.FcoeConfig") | true | None | The FCoE configuration of the physical network adapter. |
| vmDirectPathGen2Supported | bool | true | None | Flag indicating whether the NIC supports VMDirectPath Gen 2. Note that   this is only an indicator of the capabilities of this NIC, not of the   whole host.   <p>   If the host software is not capable of VMDirectPath Gen 2,   this property will be unset, as the host cannot provide information on   the NIC capability.<br>See <a href="vim.host.Capability.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a><br> |
| vmDirectPathGen2SupportedMode | string | true | None | If <a href="vim.host.PhysicalNic.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a> is true, this property advertises   the VMDirectPath Gen 2 mode supported by this NIC (chosen from   <a href="vim.host.PhysicalNic.VmDirectPathGen2SupportedMode.md">PhysicalNicVmDirectPathGen2SupportedMode</a>).   A mode may require that the associated vSphere Distributed Switch have   a particular ProductSpec in order for network passthrough to be possible. |
| resourcePoolSchedulerAllowed | bool | true | None | Flag indicating whether the NIC allows resource pool based scheduling   for network I/O control. |
| resourcePoolSchedulerDisallowedReason | string | true | None | If <a href="vim.host.PhysicalNic.md#resourcePoolSchedulerAllowed">resourcePoolSchedulerAllowed</a> is false, this property   advertises the reason for disallowing resource scheduling on   this NIC. The reasons may be one of   <a href="vim.host.PhysicalNic.ResourcePoolSchedulerDisallowedReason.md">PhysicalNicResourcePoolSchedulerDisallowedReason</a> |
| autoNegotiateSupported | bool | true | None | If set the flag indicates if the physical network adapter supports   autonegotiate. |


