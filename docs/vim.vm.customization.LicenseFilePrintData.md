vim.vm.customization.LicenseFilePrintData
=========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The LicenseFilePrintData type maps directly to the LicenseFilePrintData key in the   <tt>sysprep.inf</tt> answer file. These values are transferred into the   <tt>sysprep.inf</tt> file that VirtualCenter stores on the target virtual disk. For   more detailed information, see the document <a href =   "http://www.microsoft.com/technet/prodtechnol/Windows2000Pro/deploy/unattend/default.mspx"   >Windows 2000 Unattended Setup Guide</a>.<br>    LicenseFilePrintData provides licensing information for Windows server operating   systems.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| autoMode | [vim.vm.customization.LicenseFilePrintData.AutoMode](vim.vm.customization.LicenseFilePrintData.AutoMode.md "vim.vm.customization.LicenseFilePrintData.AutoMode") | None | None | Server licensing mode |
| autoUsers | int | true | None | This key is valid only if AutoMode = PerServer. The integer value indicates the   number of client licenses purchased for the VirtualCenter server being   installed. |


