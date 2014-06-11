vim.dvs.DistributedVirtualPortgroup
===================================
inherits from [vim.Network](vim.Network.md "vim.Network")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> managed object  defines how hosts and virtual machines connect to a network.  A distributed virtual portgroup specifies <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a>  configuration options for the ports on a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.  A portgroup also represents a <a href="vim.Network.md">Network</a> entity in the datacenter.  <br /><br />  <ul>  <li>To configure host access by portgroup, set the portgroup in the host virtual NIC specification      (<a href="vim.host.VirtualNic.Specification.md">HostVirtualNicSpec</a>.<a href="vim.host.VirtualNic.Specification.md#portgroup">portgroup</a>).  </li><br />  <li>To configure virtual machine access by portgroup, set the portgroup      in the virtual Ethernet card backing   (<a href="vim.vm.device.VirtualEthernetCard.md">VirtualEthernetCard</a>.<a href="vim.vm.device.VirtualDevice.md#backing">backing</a>.<a href="vim.vm.device.VirtualEthernetCard.DistributedVirtualPortBackingInfo.md#port">port</a>.<a href="vim.dvs.PortConnection.md#portgroupKey">portgroupKey</a>).  </li>  </ul>  <p>  When you use a portgroup for network access, the Server will create a port according  to <a href="vim.dvs.DistributedVirtualPortgroup.md#config">config</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#type">type</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='key'>key</a> | string | None | None | Generated UUID of the portgroup. |
| <a href='config'>config</a> | [vim.dvs.DistributedVirtualPortgroup.ConfigInfo](vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md "vim.dvs.DistributedVirtualPortgroup.ConfigInfo") | None | None | Configuration of the portgroup. |
| <a href='portKeys'>portKeys</a> | string | true | None | Port keys for the set of ports in the portgroup. |


ReconfigureDVPortgroup([spec](vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md "vim.dvs.DistributedVirtualPortgroup.ConfigSpec"))
----------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
| service name | ReconfigureDVPortgroup |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if spec is not valid. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | vim.fault.ConcurrentAccess |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | vim.fault.DuplicateName |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | vim.fault.InvalidName |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the spec includes settings for any VDS feature                        that is not supported on this switch. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




DVPortgroupRollback([entityBackup](vim.dvs.EntityBackup.Config.md "vim.dvs.EntityBackup.Config"))
-------------------------------------------------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.RollbackFailure](vim.fault.RollbackFailure.md "vim.fault.RollbackFailure")

---
| service name | DVPortgroupRollback |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails. |
| [vim.fault.RollbackFailure](vim.fault.RollbackFailure.md "vim.fault.RollbackFailure") | if there is no configuration specified in entityBackup and           the previous configuration does not exist either |




