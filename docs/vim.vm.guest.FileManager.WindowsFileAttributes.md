vim.vm.guest.FileManager.WindowsFileAttributes
==============================================
inherits from [vim.vm.guest.FileManager.FileAttributes](docs/vim.vm.guest.FileManager.FileAttributes.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Different attributes for a Windows guest file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hidden | bool | true | None | The file is hidden.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.WindowsFileAttributes.md">GuestWindowsFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the file will not be set as a hidden file. |
| readOnly | bool | true | None | The file is read-only.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.WindowsFileAttributes.md">GuestWindowsFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the file will not be set as a read-only file. |
| createTime | datetime | true | None | The date and time the file was created.  This property gives information about files when returned from  <a href="vim.vm.guest.FileManager.md#listFiles">ListFilesInGuest</a> or  <a href="vim.vm.guest.FileManager.md#initiateFileTransferFromGuest">InitiateFileTransferFromGuest</a>  as part of a <a href="vim.vm.guest.FileManager.WindowsFileAttributes.md">GuestWindowsFileAttributes</a>  object.  This property will be ignored when passing a  <a href="vim.vm.guest.FileManager.WindowsFileAttributes.md">GuestWindowsFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a> or  <a href="vim.vm.guest.FileManager.md#changeFileAttributes">ChangeFileAttributesInGuest</a>. |


