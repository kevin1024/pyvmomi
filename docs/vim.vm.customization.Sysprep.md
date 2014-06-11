vim.vm.customization.Sysprep
============================
inherits from [vim.vm.customization.IdentitySettings](docs/vim.vm.customization.IdentitySettings.md)


An object representation of a Windows <tt>sysprep.inf</tt> answer file. The sysprep   type encloses all the individual keys listed in a <tt>sysprep.inf</tt> file. For   more detailed information, see the document <a href =   "http://www.microsoft.com/technet/prodtechnol/Windows2000Pro/deploy/unattend/default.mspx"   >Windows 2000 Unattended Setup Guide</a>.<br>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| guiUnattended | [vim.vm.customization.GuiUnattended](vim.vm.customization.GuiUnattended.md "vim.vm.customization.GuiUnattended") | None | None | An object representation of the sysprep GuiUnattended key. |
| userData | [vim.vm.customization.UserData](vim.vm.customization.UserData.md "vim.vm.customization.UserData") | None | None | An object representation of the sysprep UserData key. |
| guiRunOnce | [vim.vm.customization.GuiRunOnce](vim.vm.customization.GuiRunOnce.md "vim.vm.customization.GuiRunOnce") | true | None | An object representation of the sysprep GuiRunOnce key. |
| identification | [vim.vm.customization.Identification](vim.vm.customization.Identification.md "vim.vm.customization.Identification") | None | None | An object representation of the sysprep Identification key. |
| licenseFilePrintData | [vim.vm.customization.LicenseFilePrintData](vim.vm.customization.LicenseFilePrintData.md "vim.vm.customization.LicenseFilePrintData") | true | None | An object representation of the sysprep LicenseFilePrintData key. Required only   for Windows 2000 Server and Windows Server 2003. |


