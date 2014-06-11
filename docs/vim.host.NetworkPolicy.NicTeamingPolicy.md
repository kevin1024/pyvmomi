vim.host.NetworkPolicy.NicTeamingPolicy
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Policy for a network adapter team.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| policy | string | true | None | Network adapter teaming policy includes failover and load balancing,   It can be one of the following:   <p>   <ul>   <li><b>loadbalance_ip</b>: route based on ip hash.   <li><b>loadbalance_srcmac</b>: route based on source MAC hash.   <li><b>loadbalance_srcid</b>: route based on the source of the port ID.   <li><b>failover_explicit</b>: use explicit failover order.   </ul>   </p><br>See <a href="vim.host.NetCapabilities.md#nicTeamingPolicy">nicTeamingPolicy</a><br> |
| reversePolicy | bool | true | None | The flag to indicate whether or not the teaming policy is applied    to inbound frames as well.   For example, if the policy is explicit failover, a broadcast request goes   through uplink1 and comes back through uplink2.  Then if the   reverse policy is set, the frame is dropped when it is    received from   uplink2. This reverse policy is useful to prevent the virtual machine    from getting reflections. |
| notifySwitches | bool | true | None | Flag to specify whether or not to notify the physical switch  if a link fails. If this property is true, ESX Server will  respond to the failure by sending a RARP packet from a different  physical adapter, causing the switch to update its cache. |
| rollingOrder | bool | true | None | The flag to indicate whether or not to use a rolling policy when  restoring links. For example, assume the explicit link order is  (vmnic9, vmnic0), therefore vmnic9 goes down, vmnic0 comes  up. However, when vmnic9 comes backup, if rollingOrder is set  to be true, vmnic0 continues to be used, otherwise, vmnic9  is restored as specified in the explicitly order. |
| failureCriteria | [vim.host.NetworkPolicy.NicFailureCriteria](vim.host.NetworkPolicy.NicFailureCriteria.md "vim.host.NetworkPolicy.NicFailureCriteria") | true | None | Failover detection policy for this network adapter team.   The bridge must be BondBridge for this property to be valid. |
| nicOrder | [vim.host.NetworkPolicy.NicOrderPolicy](vim.host.NetworkPolicy.NicOrderPolicy.md "vim.host.NetworkPolicy.NicOrderPolicy") | true | None | Failover order policy for network adapters on this switch.   The bridge must be BondBridge for this property to be valid. |


