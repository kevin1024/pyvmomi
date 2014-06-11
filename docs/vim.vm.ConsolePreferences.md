vim.vm.ConsolePreferences
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Preferences for the legacy console application that affect the way it behaves during power  operations on the virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| powerOnWhenOpened | bool | true | None | Power on the virtual machine when it is opened in the console. |
| enterFullScreenOnPowerOn | bool | true | None | Enter full screen mode when this virtual machine is powered on. |
| closeOnPowerOffOrSuspend | bool | true | None | Close the console application when the virtual machine is powered off  or suspended. |


