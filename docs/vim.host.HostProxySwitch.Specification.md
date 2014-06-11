vim.host.HostProxySwitch.Specification
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type describes the HostProxySwitch specification    representing the properties on a HostProxySwitch that can be    configured once the object exists.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| backing | [vim.dvs.HostMember.Backing](vim.dvs.HostMember.Backing.md "vim.dvs.HostMember.Backing") | true | None | The specification describes how physical network adapters   are bridged to the switch. |


