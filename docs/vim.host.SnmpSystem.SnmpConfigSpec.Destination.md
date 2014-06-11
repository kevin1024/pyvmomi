vim.host.SnmpSystem.SnmpConfigSpec.Destination
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Defines a receiver for SNMP Notifications

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostName | string | None | None | A system listening for SNMP notifications.              These must be a IPv4 unicast address or resolvable dns name. |
| port | int | None | None | UDP port to Notification receiver is listening on. udp/162 is           the reserved port |
| community | string | None | None |  |


