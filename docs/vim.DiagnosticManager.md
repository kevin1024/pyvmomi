vim.DiagnosticManager
=====================


Provides an interface to get low-level debugging logs or diagnostic bundles   for a server. For VirtualCenter, this includes the log files   for the server daemon. For an ESX Server host, this includes detailed   log files for the VMkernel.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryDescriptions([host](vim.HostSystem.md "vim.HostSystem"))
-------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryDescriptions |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Diagnostics |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the host does not exist or is specified on                a host. |




BrowseDiagnosticLog([host](vim.HostSystem.md "vim.HostSystem"), [key](#string "string"))
----------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile")

---
| service name | BrowseDiagnosticLog |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Diagnostics |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CannotAccessFile](vim.fault.CannotAccessFile.md "vim.fault.CannotAccessFile") | if the key refers to a file that cannot be accessed at                           the present time. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the key refers to a nonexistent log file or                           the log file is not of type "plain". |




GenerateLogBundles([host](vim.HostSystem.md "vim.HostSystem"))
--------------------------------------------------------------
 raises [vim.fault.LogBundlingFailed](vim.fault.LogBundlingFailed.md "vim.fault.LogBundlingFailed"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | GenerateLogBundles |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Global.Diagnostics |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.LogBundlingFailed](vim.fault.LogBundlingFailed.md "vim.fault.LogBundlingFailed") | if generation of support bundle failed. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is a pending request to generate a support bundle.    <p>   The caller can download the bundles using an HTTP GET operation   for each returned URL. Bundles are usually available for at least 24   hours, but the caller should not assume that the returned URLs are   valid indefinitely. Servers often automatically delete generated   diagnostic bundles after some given period of time. |




