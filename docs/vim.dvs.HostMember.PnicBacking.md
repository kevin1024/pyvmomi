vim.dvs.HostMember.PnicBacking
==============================
inherits from [vim.dvs.HostMember.Backing](docs/vim.dvs.HostMember.Backing.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.HostMember.PnicBacking.md">DistributedVirtualSwitchHostMemberPnicBacking</a> data object  specifies a set of physical NICs to use for a proxy switch.  When you add a host to a distributed virtual switch  (<a href="vim.dvs.HostMember.ConfigSpec.md">DistributedVirtualSwitchHostMemberConfigSpec</a>.<a href="vim.dvs.HostMember.ConfigSpec.md#host">host</a>),  the host creates a proxy switch that will use the pNICs as uplinks.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| pnicSpec | [vim.dvs.HostMember.PnicSpec](vim.dvs.HostMember.PnicSpec.md "vim.dvs.HostMember.PnicSpec") | true | None | List of physical NIC specifications. Each entry identifies  a pNIC to the proxy switch and optionally specifies uplink  portgroup and port connections for the pNIC. |


