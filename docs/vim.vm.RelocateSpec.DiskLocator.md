vim.vm.RelocateSpec.DiskLocator
===============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The DiskLocator data object type specifies a virtual disk device (by ID) and   a datastore locator for the disk's storage.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| diskId | int | None | None | Device ID of the virtual disk. |
| datastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | None | None | Target datastore. |
| diskMoveType | string | true | None | Manner in which to move the virtual disk to the <a href="vim.vm.RelocateSpec.DiskLocator.md#datastore">target datastore</a>.  The set of possible values is described   in <a href="vim.vm.RelocateSpec.DiskMoveOptions.md">VirtualMachineRelocateDiskMoveOptions</a>.   <p>   This property can only be set if <a href="vim.host.Capability.md#deltaDiskBackingsSupported">deltaDiskBackingsSupported</a> is true.   <p>   If left unset then <a href="vim.vm.RelocateSpec.DiskMoveOptions.md#moveAllDiskBackingsAndDisallowSharing">moveAllDiskBackingsAndDisallowSharing</a>   is assumed. |
| diskBackingInfo | [vim.vm.device.VirtualDevice.BackingInfo](vim.vm.device.VirtualDevice.BackingInfo.md "vim.vm.device.VirtualDevice.BackingInfo") | true | None | Backing information for the virtual disk at the destination.  This can be used, for instance, to change the format of the  virtual disk. If the specified backing is invalid or not  supported at the destination, <a href="vim.fault.InvalidDeviceBacking.md">InvalidDeviceBacking</a> is thrown. Specific property  changes may be ignored if they are not supported.  <p>  Supported BackingInfo types and properties:  <ul>  <li><a href="vim.vm.device.VirtualDisk.FlatVer2BackingInfo.md">VirtualDiskFlatVer2BackingInfo</a>    <ul>    <li>thinProvisioned    <li>eagerlyScrub    </ul>  </li>  <li><a href="vim.vm.device.VirtualDisk.SeSparseBackingInfo.md">VirtualDiskSeSparseBackingInfo</a>  (ESX 5.1 or later)  </li>  </ul> |
| profile | [vim.vm.ProfileSpec](vim.vm.ProfileSpec.md "vim.vm.ProfileSpec") | true | None | Virtual Disk Profile requirement.   Profiles are solution specific.   Profile Based Storage Management is a vSphere server extension.  The API users who want to provision VMs using Storage Profiles, need to  interact with it.   This is an optional parameter and if user doesn't specify profile,  the default behavior will apply. |


