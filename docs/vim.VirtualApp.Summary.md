vim.VirtualApp.Summary
======================
inherits from [vim.ResourcePool.Summary](docs/vim.ResourcePool.Summary.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This data object type encapsulates a typical set of resource   pool information that is useful for list views and summary pages.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| product | [vim.vApp.ProductInfo](vim.vApp.ProductInfo.md "vim.vApp.ProductInfo") | true | None | Product information. References to properties in the URLs are expanded. |
| vAppState | [vim.VirtualApp.VAppState](vim.VirtualApp.VAppState.md "vim.VirtualApp.VAppState") | true | None | Whether the vApp is running |
| suspended | bool | true | None | Whether a vApp is suspended, in the process of being suspended, or in the   process of being resumed. A stopped vApp is marked as suspended    under the following conditions:    <ul>   <li>All child virtual machines are either suspended or powered-off.</li>   <li>There is at least one suspended virtual machine for which the       stop action is not "suspend".</li>                 </ul>          If the vAppState property is "stopped", the value is set to true if the vApp is    suspended (according the the above definition).   <p>   If the vAppState property is "stopping" or "starting" and the suspend flag is set to   true, then the vApp is either in the process of being suspended or resumed   from a suspended state, respectively.   <p>   If the vAppState property is "started", then the suspend flag is set to false. |
| installBootRequired | bool | true | None | Whether one or more VMs in this vApp require a reboot to finish  installation. |
| instanceUuid | string | true | None | vCenter-specific UUID of the vApp |


