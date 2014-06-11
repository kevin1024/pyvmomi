vim.vm.customization.GuiRunOnce
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The commands listed in the GuiRunOnce data object type are executed when a user   logs on the first time after customization completes. The logon may be driven by   the <a href="vim.vm.customization.GuiUnattended.md#autoLogon">AutoLogon</a> setting.   <p>   The GuiRunOnce data object type maps to the GuiRunOnce key in the   <tt>sysprep.inf</tt> answer file. These values are transferred into the   <tt>sysprep.inf</tt> file that VirtualCenter stores on the target virtual disk. For   more detailed information, see the document <a href =  "http://www.microsoft.com/technet/prodtechnol/Windows2000Pro/deploy/unattend/default.mspx"   >Windows 2000 Unattended Setup Guide</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| commandList | string | None | None | A list of commands to run at first user logon, after guest customization. |


