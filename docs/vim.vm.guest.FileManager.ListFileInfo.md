vim.vm.guest.FileManager.ListFileInfo
=====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| files | [vim.vm.guest.FileManager.FileInfo](vim.vm.guest.FileManager.FileInfo.md "vim.vm.guest.FileManager.FileInfo") | true | None | A list of <a href="vim.vm.guest.FileManager.FileInfo.md">GuestFileInfo</a>  data objects containing information for all the matching files. |
| remaining | int | None | None | The number of files left to be returned.  If non-zero,  then the next set of files can be returned by calling  ListFiles again with the index set to the number of results  already returned. |


