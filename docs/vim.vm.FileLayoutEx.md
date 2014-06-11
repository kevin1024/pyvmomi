vim.vm.FileLayoutEx
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Detailed description of files that make up a virtual machine on disk. The   file layout is broken into 4 major sections:   <ul>   <li>Configuration: Files stored in the configuration directory   <li>Log: Files stored in the log directory   <li>Disk: Files stored relative to a disk configuration file   <li>Snapshot: Stored in the snapshot directory   </ul>   Often the same directory is used for configuration, log, disk and   snapshots.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| file | [vim.vm.FileLayoutEx.FileInfo](vim.vm.FileLayoutEx.FileInfo.md "vim.vm.FileLayoutEx.FileInfo") | true | None | Information about all the files that constitute the virtual machine   including configuration files, disks, swap file, suspend file, log files,   core files, memory file etc. <a href="vim.vm.FileLayoutEx.FileType.md">VirtualMachineFileLayoutExFileType</a> lists the   different file-types that make a virtual machine. |
| disk | [vim.vm.FileLayoutEx.DiskLayout](vim.vm.FileLayoutEx.DiskLayout.md "vim.vm.FileLayoutEx.DiskLayout") | true | None | Layout of each virtual disk attached to the virtual machine.   <p>   For a virtual machine with snaphots, this property gives only those disks   that are attached to it at the current point of running. |
| snapshot | [vim.vm.FileLayoutEx.SnapshotLayout](vim.vm.FileLayoutEx.SnapshotLayout.md "vim.vm.FileLayoutEx.SnapshotLayout") | true | None | Layout of each snapshot of the virtual machine. |
| timestamp | datetime | None | None | Time when values in this structure were last updated. |


