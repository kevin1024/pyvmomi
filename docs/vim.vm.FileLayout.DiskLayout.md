vim.vm.FileLayout.DiskLayout
============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Enumerats the set of files for each virtual disk.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | Identification of the disk in <a href="vim.vm.ConfigInfo.md">config</a>. |
| diskFile | string | None | None | List of files that makes up the virtual disk. At least one entry   always exists in this array. The first entry is the main   descriptor of the virtual disk (the one used when adding the   disk to a virtual machine). These are complete datastore paths, not   relative paths. |


