vim.dvs.DistributedVirtualPort
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a> data object represents a port in a   <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>. Virtual ports are part of a distributed   virtual portgroup. Servers create virtual ports according to the portgroup type   (<a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.<a href="vim.dvs.DistributedVirtualPortgroup.md#config">config</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#type">type</a>).   See <a href="vim.dvs.DistributedVirtualPortgroup.PortgroupType.md">DistributedVirtualPortgroupPortgroupType</a>.<br />   <ul>   <li>To configure host network access by port, set the distributed virtual port   in the host virtual NIC specification   (<a href="vim.host.VirtualNic.Specification.md">HostVirtualNicSpec</a>.<a href="vim.host.VirtualNic.Specification.md#distributedVirtualPort">distributedVirtualPort</a>.<a href="vim.dvs.PortConnection.md#portKey">portKey</a>).    </li><br />    <li>To configure virtual machine network access by port, set the port    in the virtual Ethernet card backing    (<a href="vim.vm.device.VirtualEthernetCard.md">VirtualEthernetCard</a>.<a href="vim.vm.device.VirtualDevice.md#backing">backing</a>.<a href="vim.vm.device.VirtualEthernetCard.DistributedVirtualPortBackingInfo.md#port">port</a>.<a href="vim.dvs.PortConnection.md#portKey">portKey</a>).   </li>   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Port key. |
| config | [vim.dvs.DistributedVirtualPort.ConfigInfo](vim.dvs.DistributedVirtualPort.ConfigInfo.md "vim.dvs.DistributedVirtualPort.ConfigInfo") | None | None | Port configuration, including identifying information, network  settings, and the set of entities that can connect to the port. |
| dvsUuid | string | None | None | UUID of the <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a> to which the port belongs. |
| portgroupKey | string | true | None | Key of the portgroup <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> to which  the port belongs, if any. |
| proxyHost | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | <a href="vim.HostSystem.md">HostSystem</a> that services this port. |
| connectee | [vim.dvs.PortConnectee](vim.dvs.PortConnectee.md "vim.dvs.PortConnectee") | true | None | Entity that connects to the port. |
| conflict | bool | None | None | Specifies whether the port is a conflict port. A port could be marked   as conflict if an entity is discovered connecting to a port that is   already occupied, or if the host creates a port without conferring   with vCenter Server.   <p>   The distributed virtual switch does not persist the runtime state   of a conflict port. Also, the port cannot move away from the host.   vCenter Server will not move a virtual machine (VMotion) that is   using a conflict port. |
| conflictPortKey | string | true | None | If the port is marked conflict in the case of two entities connecting to   the same port (see   <a href="vim.dvs.DistributedVirtualPort.md#conflict">conflict</a>), this is the   key of the port which the connected entity is contending for. |
| state | [vim.dvs.DistributedVirtualPort.State](vim.dvs.DistributedVirtualPort.State.md "vim.dvs.DistributedVirtualPort.State") | true | None | Runtime state of the port. |
| connectionCookie | int | true | None | Cookie representing the current instance of association between a   port and a virtual or physical NIC. See <a href="vim.dvs.PortConnection.md">DistributedVirtualSwitchPortConnection</a>.   The same cookie is present in the physical or virtual NIC configuration   (<a href="vim.dvs.PortConnection.md">DistributedVirtualSwitchPortConnection</a>.<a href="vim.dvs.PortConnection.md#connectionCookie">connectionCookie</a>)   so that the Server can verify that the entity is the rightful   connectee of the port. |
| lastStatusChange | datetime | None | None | The last time the  <a href="vim.dvs.DistributedVirtualPort.md#state">state</a>.<a href="vim.dvs.DistributedVirtualPort.State.md#runtimeInfo">runtimeInfo</a>   value was changed. |
| hostLocalPort | bool | true | None | Specifies whether the port is a host local port. A host local port is  created   to resurrect the management network connection on a VMkernel virtual NIC.   You cannot use vCenter Server to reconfigure this port and you cannot   reassign the port. |


