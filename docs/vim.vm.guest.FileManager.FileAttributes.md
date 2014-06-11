vim.vm.guest.FileManager.FileAttributes
=======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Different attributes for a guest file.  <p>  <ul>     <li> Check <a href="vim.vm.guest.FileManager.PosixFileAttributes.md">GuestPosixFileAttributes</a>          for Posix guest files.</li>     <li> Check <a href="vim.vm.guest.FileManager.WindowsFileAttributes.md">GuestWindowsFileAttributes</a>          for Windows guest files.</li>  </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| modificationTime | datetime | true | None | The date and time the file was last modified.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.FileAttributes.md">GuestFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the default value will be the time when the file is created inside the  guest. |
| accessTime | datetime | true | None | The date and time the file was last accessed.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.FileAttributes.md">GuestFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the default value will be the time when the file is created inside the  guest. |
| symlinkTarget | string | true | None | The target for the file if it's a symbolic link.  This is currently only set for Linux guest operating systems,  but may be supported in the  future on Windows guest operating systems that support symbolic links.  This property gives information about files when returned from  <a href="vim.vm.guest.FileManager.md#listFiles">ListFilesInGuest</a> or  <a href="vim.vm.guest.FileManager.md#initiateFileTransferFromGuest">InitiateFileTransferFromGuest</a>  as part of a <a href="vim.vm.guest.FileManager.FileAttributes.md">GuestFileAttributes</a> object.  This property will be ignored when passing a  <a href="vim.vm.guest.FileManager.FileAttributes.md">GuestFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a> or  <a href="vim.vm.guest.FileManager.md#changeFileAttributes">ChangeFileAttributesInGuest</a>. |


