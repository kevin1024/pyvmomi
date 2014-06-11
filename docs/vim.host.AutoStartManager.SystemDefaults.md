vim.host.AutoStartManager.SystemDefaults
========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Defines the system default auto-start/auto-stop values.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| enabled | bool | true | None | Indicates whether or not auto-start manager is enabled. |
| startDelay | int | true | None | System-default autoStart delay in seconds. The default is 120 seconds. |
| stopDelay | int | true | None | System-default autoStop delay in seconds. The default is 120 seconds. |
| waitForHeartbeat | bool | true | None | System-default waitForHeartbeat setting. |
| stopAction | string | true | None | System-default power-off action. Used if the stopAction string in the   AutoPowerInfo object for a particular machine is set to systemDefault.   If stopAction and startAction for a virtual machine are both set to none,   that virtual machine is removed from the AutoStart sequence. |


