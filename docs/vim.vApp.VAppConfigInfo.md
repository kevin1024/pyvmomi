vim.vApp.VAppConfigInfo
=======================
inherits from [vim.vApp.VmConfigInfo](docs/vim.vApp.VmConfigInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Configuration of a vApp container.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entityConfig | [vim.vApp.EntityConfigInfo](vim.vApp.EntityConfigInfo.md "vim.vApp.EntityConfigInfo") | true | None | Configuration of sub-entities (virtual machine or vApp). |
| annotation | string | None | None | Description for the vApp. |
| instanceUuid | string | true | None | vCenter-specific 128-bit UUID of a vApp, represented  as a hexademical    string. This identifier is used by vCenter to uniquely identify all    vApp instances. |
| managedBy | [vim.ext.ManagedByInfo](vim.ext.ManagedByInfo.md "vim.ext.ManagedByInfo") | true | None | Specifies that this vApp is managed by a VC Extension. See the  <a href="vim.vApp.VAppConfigSpec.md#managedBy">managedBy</a> property in the  VAppConfigSpec for more details. |


