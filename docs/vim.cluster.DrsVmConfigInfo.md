vim.cluster.DrsVmConfigInfo
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


DRS configuration for a single virtual machine. This makes it possible   to override the default behavior for an individual virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | None | None | Reference to the virtual machine. |
| enabled | bool | true | None | Flag to indicate whether or not VirtualCenter is allowed to perform any   DRS migration or initial placement recommendations for this virtual   machine.   If this flag is false, the virtual machine is effectively excluded from   DRS.   <p>   If no individual DRS specification exists for a virtual machine,   this property defaults to true. |
| behavior | [vim.cluster.DrsConfigInfo.DrsBehavior](vim.cluster.DrsConfigInfo.DrsBehavior.md "vim.cluster.DrsConfigInfo.DrsBehavior") | true | None | Specifies the particular DRS behavior for this virtual machine.<br>See <a href="vim.cluster.DrsConfigInfo.md">ClusterDrsConfigInfo</a><br> |


