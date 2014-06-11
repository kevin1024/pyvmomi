vim.vm.guest.FileManager.PosixFileAttributes
============================================
inherits from [vim.vm.guest.FileManager.FileAttributes](docs/vim.vm.guest.FileManager.FileAttributes.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


Different attributes for Posix guest file.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ownerId | int | true | None | The owner ID.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.PosixFileAttributes.md">GuestPosixFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the default value will be the owner Id of the user who invoked  the file transfer operation. |
| groupId | int | true | None | The group ID.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.PosixFileAttributes.md">GuestPosixFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the default value will be the group Id of the user who invoked  the file transfer operation. |
| permissions | long | true | None | The file permissions in chmod(2) format.  If this property is not specified when passing a  <a href="vim.vm.guest.FileManager.PosixFileAttributes.md">GuestPosixFileAttributes</a> object to  <a href="vim.vm.guest.FileManager.md#initiateFileTransferToGuest">InitiateFileTransferToGuest</a>,  the file will be created with 0644 permissions. |


