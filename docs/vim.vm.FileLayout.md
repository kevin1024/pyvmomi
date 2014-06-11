vim.vm.FileLayout
=================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
### DEPRECATED



Describes the set of files that makes up a virtual machine on disk. The   file layout is broken into 4 major sections:   <ul>   <li>Configuration: Files stored in the configuration directory   <li>Log: Files stored in the log directory   <li>Disk: Files stored relative to a disk configuration file   <li>Snapshot: Stored in the snapshot directory   </ul>   Often the same directory is used for configuration, log, disk and   snapshots.   <p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| configFile | string | true | None | A list of files that makes up the configuration of the virtual machine   (excluding the .vmx file, since that file is represented in the   FileInfo). These are relative paths from the configuration directory. A   slash is always used as a separator. This list will typically include the   NVRAM file, but could also include other meta-data files. |
| logFile | string | true | None | A list of files stored in the virtual machine's log directory. These are   relative paths from the logDirectory. A slash is always used as a   separator. |
| disk | [vim.vm.FileLayout.DiskLayout](vim.vm.FileLayout.DiskLayout.md "vim.vm.FileLayout.DiskLayout") | true | None | Files making up each virtual disk. |
| snapshot | [vim.vm.FileLayout.SnapshotLayout](vim.vm.FileLayout.SnapshotLayout.md "vim.vm.FileLayout.SnapshotLayout") | true | None | Files of each snapshot. |
| swapFile | string | true | None | The swapfile specific to this virtual machine, if any. This is a   complete datastore path, not a relative path. |


