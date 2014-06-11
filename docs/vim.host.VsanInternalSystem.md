vim.host.VsanInternalSystem
===========================
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The VsanInternalSystem exposes low level access to CMMDS, as well as draft  versions of VSAN object and disk management APIs that are subject to change  in future releases. No compatibility is guaranteed on any of the APIs,  including their prototype, behavior or result encoding.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryCmmds([queries](vim.host.VsanInternalSystem.CmmdsQuery.md "vim.host.VsanInternalSystem.CmmdsQuery"))
---------------------------------------------------------------------------------------------------------

| service name | QueryCmmds |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




QueryPhysicalVsanDisks([props](#string "string"))
-------------------------------------------------

| service name | QueryPhysicalVsanDisks |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




QueryVsanObjects([uuids](#string "string"))
-------------------------------------------

| service name | QueryVsanObjects |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




QueryObjectsOnPhysicalVsanDisk([disks](#string "string"))
---------------------------------------------------------

| service name | QueryObjectsOnPhysicalVsanDisk |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | System.Read |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




