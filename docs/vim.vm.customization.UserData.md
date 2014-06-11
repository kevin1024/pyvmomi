vim.vm.customization.UserData
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Personal data pertaining to the owner of the virtual machine.   <p>   The UserData data object type maps to the UserData key in the <tt>sysprep.inf</tt>   answer file. These values are transferred directly into the <tt>sysprep.inf</tt>   file that VirtualCenter stores on the target virtual disk. For more detailed   information, see the document <a href =   "http://www.microsoft.com/technet/prodtechnol/Windows2000Pro/deploy/unattend/default.mspx"   >Windows 2000 Unattended Setup Guide</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| fullName | string | None | None | User's full name. |
| orgName | string | None | None | User's organization. |
| computerName | [vim.vm.customization.NameGenerator](vim.vm.customization.NameGenerator.md "vim.vm.customization.NameGenerator") | None | None | The computer name of the (Windows) virtual machine. Computer name may contain  letters (A-Z), numbers(0-9) and hyphens (-) but no spaces or periods (.).  The name may not consists entirely of digits.   On Vista computer name is restricted to 15 characters in length. If the computer  name is longer than 15 characters, it will be truncated to 15 characters. |
| productId | string | None | None | Microsoft Sysprep requires that a valid serial number be included in the answer   file when mini-setup runs. This serial number is ignored if the original guest   operating system was installed using a volume-licensed CD. |


