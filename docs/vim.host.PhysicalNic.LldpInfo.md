vim.host.PhysicalNic.LldpInfo
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The Link Layer Discovery Protocol information.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| chassisId | string | None | None | ChassisId represents the chassis identification for the device that   transmitted the LLDP frame. The receiving LLDP agent combines the   Chassis ID and portId to represent the entity connected to the port   where the frame was received. |
| portId | string | None | None | This property identifies the specific port that transmitted the LLDP   frame. The receiving LLDP agent combines the Chassis ID and Port to   represent the entity connected to the port where the frame was received. |
| timeToLive | int | None | None | It is the duration of time in seconds for which information contained   in the received LLDP frame shall be valid. If a value of zero is sent   it can also identify a device that has shut down or is no longer   transmitting, prompting deletion of the record from the local database. |
| parameter | [vmodl.KeyAnyValue](vmodl.KeyAnyValue.md "vmodl.KeyAnyValue") | true | None | LLDP parameters |


