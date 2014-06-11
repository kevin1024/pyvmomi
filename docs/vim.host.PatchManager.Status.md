vim.host.PatchManager.Status
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Unique identifier for this update. |
| applicable | bool | None | None | Whether or not this update is applicable to this host. An update   may not be applicable to the ESX host for many reasons--for   example, it is obsolete, it conflicts with other installed   patches or libraries, and so on. The <a href="vim.host.PatchManager.Status.md#reason">reason</a> shows some of the reasons   why the update is not applicable.    An update could be inapplicable with no reason listed. This is   because the prerequisite install state is not correct. For example,   update A is one of the prerequisites of update B. B not only   requires A to be installed, but also requires the host is   rebooted after A is installed. When A is installed and the host   has not been restarted after the installation, B will not be   applicable. In such a case, the scan on both updates A and B   would yield a whole picture of the update applicable status. |
| reason | string | true | None | Possible reasons why an update is not applicable to the ESX host.<br>See <a href="vim.host.PatchManager.Status.Reason.md">HostPatchManagerReason</a><br> |
| integrity | string | true | None | The integrity status of the update's metadata. The value would   be unset if the integrity status is unknown to the server.<br>See <a href="vim.host.PatchManager.Status.Integrity.md">HostPatchManagerIntegrityStatus</a><br> |
| installed | bool | None | None | Whether the update is installed on the server. |
| installState | string | true | None | The installation state of the update. Unset if the update is not   installed on the server.<br>See <a href="vim.host.PatchManager.Status.InstallState.md">HostPatchManagerInstallState</a><br> |
| prerequisitePatch | [vim.host.PatchManager.Status.PrerequisitePatch](vim.host.PatchManager.Status.PrerequisitePatch.md "vim.host.PatchManager.Status.PrerequisitePatch") | true | None | Prerequisite update. |
| restartRequired | bool | None | None | Whether or not this update requires a host restart to take effect. |
| reconnectRequired | bool | None | None | Whether or not this update requires caller to reconnect to the   host. This is usually because the update is on the agent that   running on the host, the agent would thus be restarted when the   update is applied. Caller can reconnect (and possibly relogin) to   the host after the agent has been restarted. |
| vmOffRequired | bool | None | None | Whether or not this update requires the host in maintenance mode. |
| supersededPatchIds | string | true | None | Patches that are superseded by this update. |


