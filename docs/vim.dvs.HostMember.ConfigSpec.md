vim.dvs.HostMember.ConfigSpec
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Specification to create or reconfigure ESXi host membership  in a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operation | string | None | None | Host member operation type. See   <a href="vim.ConfigSpecOperation.md">ConfigSpecOperation</a> for valid values. |
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | Identifies a host member of a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>  for a <a href="vim.Folder.md#createDistributedVirtualSwitch">CreateDVS_Task</a> or  <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.<a href="vim.DistributedVirtualSwitch.md#reconfigure">ReconfigureDvs_Task</a> operation. |
| backing | [vim.dvs.HostMember.Backing](vim.dvs.HostMember.Backing.md "vim.dvs.HostMember.Backing") | true | None | Specifies the physical NICs to use as backing for the proxy switch   on the host. |
| maxProxySwitchPorts | int | true | None | Maximum number of ports allowed in the <a href="vim.host.HostProxySwitch.md">HostProxySwitch</a>.  <p>  <i>ESXi 5.0 and earlier hosts</i>: If you are reconfiguring an existing  host membership, that is, the proxy switch already exists, you must reboot  the host for the new setting to take effect. |
| vendorSpecificConfig | [vim.dvs.KeyedOpaqueBlob](vim.dvs.KeyedOpaqueBlob.md "vim.dvs.KeyedOpaqueBlob") | true | None | Opaque binary blob that stores vendor specific configuration. |


