vim.host.VsanSystem
===================
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The VsanSystem managed object type exposes VSAN configuration  primitives and serves as a host-level access point for relevant  VSAN data objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='config'>config</a> | [vim.vsan.host.ConfigInfo](vim.vsan.host.ConfigInfo.md "vim.vsan.host.ConfigInfo") | None | System.Read | The current VSAN service configuration information for this host. |


QueryDisksForVsan([canonicalName](#string "string"))
----------------------------------------------------

| service name | QueryDisksForVsan |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AddDisks([disk](vim.host.ScsiDisk.md "vim.host.ScsiDisk"))
----------------------------------------------------------

| service name | AddDisks |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




InitializeDisks([mapping](vim.vsan.host.DiskMapping.md "vim.vsan.host.DiskMapping"))
------------------------------------------------------------------------------------

| service name | InitializeDisks |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




RemoveDisk([disk](vim.host.ScsiDisk.md "vim.host.ScsiDisk"))
------------------------------------------------------------

| service name | RemoveDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




RemoveDiskMapping([mapping](vim.vsan.host.DiskMapping.md "vim.vsan.host.DiskMapping"))
--------------------------------------------------------------------------------------

| service name | RemoveDiskMapping |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




UpdateVsan([config](vim.vsan.host.ConfigInfo.md "vim.vsan.host.ConfigInfo"))
----------------------------------------------------------------------------

| service name | UpdateVsan |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




QueryHostStatus()
-----------------

| service name | QueryHostStatus |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




