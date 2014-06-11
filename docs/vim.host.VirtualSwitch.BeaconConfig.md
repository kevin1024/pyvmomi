vim.host.VirtualSwitch.BeaconConfig
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the configuration of the beacon   to probe connectivity of physical network adapters.  A   beacon is sent out of one network adapter and should arrive on another   network adapter in the team.  The successful roundtrip indicates   that the network adapters are working.   <p>   Define this data object to enable beacon probing as a method to validate   the link status of a physical network adapter.  Beacon probing must   be configured in order to use the beacon status as a criteria to   determine if a physical network adapter failed.<br>See <a href="vim.host.NetworkPolicy.NicFailureCriteria.md#checkBeacon">checkBeacon</a><br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| interval | int | None | None | Determines how often, in seconds, a beacon should be sent. |


