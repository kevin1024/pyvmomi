vim.vm.guest.ProcessManager.ProcessInfo
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The process name |
| pid | long | None | None | The process ID |
| owner | string | None | None | The process owner |
| cmdLine | string | None | None | The full command line |
| startTime | datetime | None | None | The start time of the process |
| endTime | datetime | true | None | If the process was started using  <a href="vim.vm.guest.ProcessManager.md#startProgram">StartProgramInGuest</a>  then the process completion time will be available if  queried within 5 minutes after it completes. |
| exitCode | int | true | None | If the process was started using  <a href="vim.vm.guest.ProcessManager.md#startProgram">StartProgramInGuest</a>  then the process exit code will be available if  queried within 5 minutes after it completes. |


