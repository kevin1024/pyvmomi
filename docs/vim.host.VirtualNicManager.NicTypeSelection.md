vim.host.VirtualNicManager.NicTypeSelection
===========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


DataObject which lets a VirtualNic be marked for  use as a <a href="vim.host.VirtualNicManager.NicType.md">HostVirtualNicManagerNicType</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| vnic | [vim.host.VirtualNicConnection](vim.host.VirtualNicConnection.md "vim.host.VirtualNicConnection") | None | None | VirtualNic for the selection is being made |
| nicType | string | true | None |  |


