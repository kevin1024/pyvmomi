vim.host.PatchManager.Status.PrerequisitePatch
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Updates that are required to be installed before this update can   be installed on the server.    In addition to being installed on the server, an update can have   additional requirement on the server or services running on the   server pertaining to the prerequisite update.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Unique identifier of the prerequisite update. |
| installState | string | true | None | The requirement on the server or services running on the   server pertaining to the prerequisite update. For example,   this update could require the server to be rebooted after the   prerequisite update is installed. Unset if there is no   additional requirement on the prerequisite update.<br>See <a href="vim.host.PatchManager.Status.InstallState.md">HostPatchManagerInstallState</a><br> |


