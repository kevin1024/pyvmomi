vim.vApp.VAppConfigSpec
=======================
inherits from [vim.vApp.VmConfigSpec](docs/vim.vApp.VmConfigSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Configuration of a vApp

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| entityConfig | [vim.vApp.EntityConfigInfo](vim.vApp.EntityConfigInfo.md "vim.vApp.EntityConfigInfo") | true | None | Configuration of sub-entities (virtual machine or vApp container).  <p>  Reconfigure privilege: See EntityConfigInfo |
| annotation | string | true | None | Description for the vApp.  <p>  Reconfigure privilege: VApp.Rename. |
| instanceUuid | string | true | None | vCenter-specific 128-bit UUID of a vApp, represented as a hexadecimal   string. This identifier is used  by vCenter to uniquely identify all    vApp instances in the Virtual Infrastructure environment.   <p>   Normally, this property is not set by a client, allowing the   Virtual Infrastructure environment to assign or change it when   VirtualCenter detects an identifier conflict between vApps.    <p>   Reconfigure privilege: VApp.ApplicationConfig |
| managedBy | [vim.ext.ManagedByInfo](vim.ext.ManagedByInfo.md "vim.ext.ManagedByInfo") | true | None | Specifies that this vApp is managed by a VC Extension.  <p>  This information is primarily used in the Client to show a custom icon for  managed vApps, and a description of the function of the vApp. If no extension  can be found with the extension key in the <a href="vim.ext.ManagedByInfo.md">managedBy</a>  object, or the type is not found in the  <a href="vim.Extension.md#managedEntityInfo">managedEntityInfo</a> list of the  extension, the default vApp icon is used, and no description is shown.  <p>  Reconfigure privilege: VApp.ApplicationConfig |


