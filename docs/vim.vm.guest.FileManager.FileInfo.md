vim.vm.guest.FileManager.FileInfo
=================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| path | string | None | None | The complete path to the file |
| type | string | None | None | The file type, one of <a href="vim.vm.guest.FileManager.FileInfo.FileType.md">GuestFileType</a> |
| size | long | None | None | The file size in bytes |
| attributes | [vim.vm.guest.FileManager.FileAttributes](vim.vm.guest.FileManager.FileAttributes.md "vim.vm.guest.FileManager.FileAttributes") | None | None | Different attributes of a file. |


