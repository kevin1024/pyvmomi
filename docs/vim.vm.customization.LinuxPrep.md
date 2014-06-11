vim.vm.customization.LinuxPrep
==============================
inherits from [vim.vm.customization.IdentitySettings](docs/vim.vm.customization.IdentitySettings.md)


This is the Linux counterpart to the Windows Sysprep object. LinuxPrep contains   machine-wide settings that identify a Linux machine in the same way that the   Sysprep type identifies a Windows machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostName | [vim.vm.customization.NameGenerator](vim.vm.customization.NameGenerator.md "vim.vm.customization.NameGenerator") | None | None | The network host name of the (Linux) virtual machine. |
| domain | string | None | None | The fully qualified domain name. |
| timeZone | string | true | None | The case-sensitive timezone, such as Europe/Sofia.   <a href="timezone.md" title="Display list of Valid timeZone values...">   <strong>Valid timeZone values</strong></a> are based on the tz (timezone)   database used by Linux and other Unix systems.   The values are strings (xsd:string) in the form "Area/Location," in which   Area is a continent or ocean name, and Location is the city, island, or   other regional designation. |
| hwClockUTC | bool | true | None | Specifies whether the hardware clock is in UTC or local time.   <ul>   <li>True when the hardware clock is in UTC.</li>   <li>False when the hardware clock is in local time.</li>   </ul> |


