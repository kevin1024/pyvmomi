vim.vm.DefaultPowerOpInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The DefaultPowerOpInfo data object type holds the configured defaults for the power   operations on a virtual machine. The properties indicated whether to do a "soft"  or guest initiated operation, or a "hard" operation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| powerOffType | string | true | None | Describes the default power off type for this virtual machine.   The possible values are specified by the PowerOpType.   <ul>  <li> hard - Perform power off by using the PowerOff method.  <li> soft - Perform power off by using the ShutdownGuest method.  <li> preset - The preset value is specified in the defaultPowerOffType        section.   </ul>  This setting is advisory and clients can choose to ignore it. |
| suspendType | string | true | None | Describes the default suspend type for this virtual machine.   The possible values are specified by the PowerOpType.   <ul>  <li> hard - Perform suspend by using the Suspend method.  <li> soft - Perform suspend by using the StandbyGuest method.  <li> preset - The preset value is specified in the defaultSuspendType       section.   </ul>  This setting is advisory and clients can choose to ignore it. |
| resetType | string | true | None | Describes the default reset type for this virtual machine.   The possible values are specified by the PowerOpType.   <ul>  <li> hard - Perform reset by using the Reset method.  <li> soft - Perform reset by using the RebootGuest method.  <li> preset - The preset value is specified in the defaultResetType       section.   </ul>  This setting is advisory and clients can choose to ignore it. |
| defaultPowerOffType | string | true | None | Default operation for power off: soft or hard |
| defaultSuspendType | string | true | None | Default operation for suspend: soft or hard |
| defaultResetType | string | true | None | Default operation for reset: soft or hard |
| standbyAction | string | true | None | Behavior of virtual machine when it receives the S1 ACPI call. |


