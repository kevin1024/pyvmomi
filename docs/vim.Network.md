vim.Network
===========
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")


Represents a network accessible by either hosts or virtual machines. This can be a   physical network or a logical network, such as a VLAN.   <p>   Networks are created:   <ul>      <li>explicitly when configuring a host.      <li>automatically when adding a host to VirtualCenter.      <li>automatically when adding a new virtual machine to a host or to          VirtualCenter.   </ul>   <p>   To configure network access for hosts and virtual machines, use   <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a> and   <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> managed objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='name'>name</a> | string | None | None | Name of this network. |
| <a href='summary'>summary</a> | [vim.Network.Summary](vim.Network.Summary.md "vim.Network.Summary") | None | None | Properties of a network. |
| <a href='host'>host</a> | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | Hosts attached to this network. |
| <a href='vm'>vm</a> | [vim.VirtualMachine](vim.VirtualMachine.md "vim.VirtualMachine") | true | None | Virtual machines using this network. |


DestroyNetwork()
----------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse")

---
### Deprecated
As of VI API 2.5 do not use this method. This method throws               <a href="vim.fault.ResourceInUse.md">ResourceInUse</a>.  Networks are automatically               removed when no longer in use, so this method is unnecessary.

| service name | DestroyNetwork |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Network.Delete |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if one or more hosts or virtual machines are configured   to use the network. |




