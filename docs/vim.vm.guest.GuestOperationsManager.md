vim.vm.guest.GuestOperationsManager
===================================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


GuestOperationsManager is the managed object that provides APIs  to manipulate the guest operating system files and process.   Each class of APIs is separated into its own manager.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='authManager'>authManager</a> | [vim.vm.guest.AuthManager](vim.vm.guest.AuthManager.md "vim.vm.guest.AuthManager") | true | System.Anonymous | A singleton managed object that provides methods for guest authentication  operations. |
| <a href='fileManager'>fileManager</a> | [vim.vm.guest.FileManager](vim.vm.guest.FileManager.md "vim.vm.guest.FileManager") | true | System.Anonymous | A singleton managed object that provides methods for guest file  operations. |
| <a href='processManager'>processManager</a> | [vim.vm.guest.ProcessManager](vim.vm.guest.ProcessManager.md "vim.vm.guest.ProcessManager") | true | System.Anonymous | A singleton managed object that provides methods for guest process  operations. |


