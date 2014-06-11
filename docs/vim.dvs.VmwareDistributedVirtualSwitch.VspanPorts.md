vim.dvs.VmwareDistributedVirtualSwitch.VspanPorts
=================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This class defines the ports, uplink ports name, vlans and IP addresses participating in a   Distributed Port Mirroring session. See VspanSession.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| portKey | string | true | None | Individual ports to participate in the Distributed Port Mirroring session. |
| uplinkPortName | string | true | None | Uplink ports used as destination ports to participate in the Distributed Port Mirroring session.   A fault will be raised if uplinkPortName is used as source ports   in any Distributed Port Mirroring session. |
| wildcardPortConnecteeType | string | true | None | Wild card specification for source ports participating in the Distributed Port Mirroring session.   See <a href="vim.dvs.PortConnectee.ConnecteeType.md">DistributedVirtualSwitchPortConnecteeConnecteeType</a> for valid values.   Any port that has a connectee of the specified type has its receive traffic   mirrored. A fault will be raised if wildcards are specified as destination   ports or source ports mirroring traffic on the transmit side.   It is to be not used. |
| vlans | int | true | None | Vlan Ids for ingress source of Remote Mirror destination   session. |
| ipAddress | string | true | None | IP address for the destination of encapsulated remote mirror source session,   IPv4 address is specified using dotted decimal notation.   For example, "192.0.2.1".   IPv6 addresses are 128-bit addresses represented as eight fields   of up to four hexadecimal digits.   A colon separates each field (:). For example,   2001:DB8:101::230:6eff:fe04:d9ff. |


