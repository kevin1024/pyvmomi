vim.host.NetworkPolicy.NicFailureCriteria
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the network adapter failover    detection algorithm for a network adapter team.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| checkSpeed | string | true | None | To use link speed as the criteria, <em>checkSpeed</em> must be one of   the following values:   <p>   <ul>   <li> <b>exact</b>: Use exact speed to detect link failure.        <b>speed</b> is the configured exact speed in megabits per second.   <li> <b>minimum</b>: Use minimum speed to detect failure.        <b>speed</b> is the configured minimum speed in megabits per second.   <li> <b>empty string</b>: Do not use link speed to detect failure.         <b>speed</b> is unused in this case.   </ul> |
| speed | int | true | None | see vim.host.NetworkPolicy.NicFailureCriteria#checkSpeed<br>See <a href="vim.host.NetworkPolicy.NicFailureCriteria.md#checkSpeed">checkSpeed</a><br> |
| checkDuplex | bool | true | None | The flag to indicate whether or not to use the link duplex reported    by the driver as link selection criteria.   <p>   If <b>checkDuplex</b> is true, then fullDuplex is the configured    duplex mode.  The link is considered bad if the link duplex reported    by driver is not the same as fullDuplex.   </p>   <p>   If <b>checkDuplex</b> is false, then fullDuplex is unused, and   link duplexity is not used as a detection method. |
| fullDuplex | bool | true | None | see vim.host.NetworkPolicy.NicFailureCriteria#checkDuplex<br>See <a href="vim.host.NetworkPolicy.NicFailureCriteria.md#checkDuplex">checkDuplex</a><br> |
| checkErrorPercent | bool | true | None | The flag to indicate whether or not to use link error percentage    to detect failure.   <p>   If <b>checkErrorPercent</b> is true, then percentage is the configured    error percentage that is tolerated.  The link is considered bad    if error rate exceeds percentage.   <p>   If <b>checkErrorPercent</b> is false, percentage is unused, and   error percentage is not used as a detection method. |
| percentage | int | true | None | see vim.host.NetworkPolicy.NicFailureCriteria#checkErrorPercent<br>See <a href="vim.host.NetworkPolicy.NicFailureCriteria.md#checkErrorPercent">checkErrorPercent</a><br> |
| checkBeacon | bool | true | None | The flag to indicate whether or not to enable this property to    enable beacon probing as a method to validate   the link status of a physical network adapter.   <p>   <b>checkBeacon</b> can be enabled only if the VirtualSwitch has been   configured to use the beacon.  Attempting to set <b>checkBeacon</b>   on a PortGroup or VirtualSwitch that does not have beacon probing   configured for the applicable VirtualSwitch results in an error.<br>See <a href="vim.host.VirtualSwitch.BondBridge.md#beacon">beacon</a><br>See <a href="vim.host.VirtualSwitch.BeaconConfig.md">HostVirtualSwitchBeaconConfig</a><br> |


