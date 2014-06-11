vim.vm.customization.WinOptions
===============================
inherits from [vim.vm.customization.Options](docs/vim.vm.customization.Options.md)


Optional operations supported by the customization process for Windows.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| changeSID | bool | None | None | The customization process should modify the machine's security identifier (SID).   For Vista OS, SID will always be modified. |
| deleteAccounts | bool | None | None | If deleteAccounts is true, then all user accounts are removed from the system as   part of the customization. Mini-setup creates a new Administrator account with a   blank password. |
| reboot | [vim.vm.customization.WinOptions.SysprepRebootOption](vim.vm.customization.WinOptions.SysprepRebootOption.md "vim.vm.customization.WinOptions.SysprepRebootOption") | true | None | A value of type SysprepRebootOption specifying the action that should be  taken after running sysprep. Defaults to "reboot". |


