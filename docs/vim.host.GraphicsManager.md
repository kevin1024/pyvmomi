vim.host.GraphicsManager
========================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This managed object manages the graphics state of the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='graphicsInfo'>graphicsInfo</a> | [vim.host.GraphicsInfo](vim.host.GraphicsInfo.md "vim.host.GraphicsInfo") | true | System.Read | Array of graphics information |


RefreshGraphicsManager()
------------------------

| service name | RefreshGraphicsManager |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Settings |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




IsSharedGraphicsActive()
------------------------

| service name | IsSharedGraphicsActive |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|




