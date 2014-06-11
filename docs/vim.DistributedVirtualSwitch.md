vim.DistributedVirtualSwitch
============================
inherits from [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


A <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a> managed object is a virtual network   switch that is located on a vCenter Server. A distributed virtual switch   manages configuration for proxy switches (<a href="vim.host.HostProxySwitch.md">HostProxySwitch</a>).   A proxy switch is located on an ESXi host that is managed by the vCenter   Server and is a member of the switch.   A distributed switch also provides virtual port state management   so that port state is maintained when vCenter Server operations   move a virtual machine from one host to another.   <p>   A proxy switch performs network I/O to support the following network traffic   and operations:   <ul>   <li>Network traffic between virtual machines on any hosts that are members   of the distributed virtual switch.</li>   <li>Network traffic between virtual machines that uses a distributed switch   and a virtual machine that uses a VMware standard switch.</li>   <li>Network traffic between a virtual machine and a remote system   on a physical network connected to the ESXi host.</li>   <li>vSphere system operations to support capabilities   such as VMotion or High Availability.</li>   </ul>   <p>   A <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a> is the base distributed   switch implementation. It supports a VMware distributed virtual   switch implementation and it supports third party distributed   switch implementations. The base implementation provides   the following capabilities   (<a href="vim.DistributedVirtualSwitch.FeatureCapability.md">DVSFeatureCapability</a>):   </p>   <ul>   <li>NIC teaming</li>   <li>Network I/O control</li>   <li>Network resource allocation</li>   <li>Quality of service tag support</li>   <li>User-defined resource pools</li>   <li>I/O passthrough (VMDirectPath Gen2)</li>   </ul>   <p>   A <a href="vim.dvs.VmwareDistributedVirtualSwitch.md">VmwareDistributedVirtualSwitch</a>   supports the following additional capabilities   (<a href="vim.DistributedVirtualSwitch.FeatureCapability.md">DVSFeatureCapability</a> and   <a href="vim.dvs.VmwareDistributedVirtualSwitch.FeatureCapability.md">VMwareDVSFeatureCapability</a>):   </p>   <ul>   <li>Backup, restore, and rollback for a VMware distributed virtual switch   and its associated portgroups.</li>   <li>Maximum Transmission Unit (MTU) configuration.</li>   <li>Health check operations for NIC teaming and VLAN/MTU support.</li>   <li>Monitoring switch traffic using Internet Protocol Flow Information Export (IPFIX).</li>   <li>Link Layer Discovery Protocol (LLDP).</li>   <li>Virtual network segmentation using a Private VLAN (PVLAN).</li>   <li>VLAN-based SPAN (VSPAN) for virtual distributed port mirroring.</li>   <li>Link Aggregation Control Protocol (LACP) defined for uplink portgroups.</li>   </ul>   <h3>Distributed Virtual Switch Configuration</h3>   <p>   To use a distributed virtual switch, you create a switch and portgroups   on a vCenter Server, and add hosts as members of the switch.   </p>   <ol>   <li>Create a distributed virtual switch   (<a href="vim.Folder.md">Folder</a>.<a href="vim.Folder.md#createDistributedVirtualSwitch">CreateDVS_Task</a>).   Use a <a href="vim.DistributedVirtualSwitch.ConfigSpec.md">DVSConfigSpec</a> to create a switch   for a third-party implementation. Use a   <a href="vim.dvs.VmwareDistributedVirtualSwitch.ConfigSpec.md">VMwareDVSConfigSpec</a> to create   a VMware distributed virtual switch.   </li><br />   <li>Create portgroups (<a href="vim.DistributedVirtualSwitch.md#addPortgroup">CreateDVPortgroup_Task</a>)   for host and virtual machine network connections and for the connection between   proxy switches and physical NICs.   A <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a> specifies how   virtual ports (<a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a>) will be used.   When you create a distributed virtual switch, the vCenter Server   automatically creates one uplink portgroup   (<a href="vim.DistributedVirtualSwitch.md#config">config</a>.<a href="vim.DistributedVirtualSwitch.ConfigInfo.md#uplinkPortgroup">uplinkPortgroup</a>).   Uplink portgroups are distributed virtual portgroups that support   the connection between proxy switches and physical NICs.   <p>   Port creation on a distributed switch is determined by the   portgroup type   (<a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md">DVPortgroupConfigSpec</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md#type">type</a>):   </p>   <ul>   <li>If a portgroup is early binding (static), then   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md">DVPortgroupConfigSpec</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md#numPorts">numPorts</a>   determines the number of ports that get created when the portgroup is created.   This number can be increased if   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md">DVPortgroupConfigSpec</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md#autoExpand">autoExpand</a>   is <code>true</code>.   </li><br />   <li>If a portgroup is ephemeral (dynamic), then   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md#numPorts">numPorts</a>   is ignored and ports are created as needed.   </li>   </ul>   <p>   You can also specify standalone ports that are not associated with   a port group and uplink ports that are created on ESXi hosts  (<a href="vim.DistributedVirtualSwitch.ConfigSpec.md">DVSConfigSpec</a>.<a href="vim.DistributedVirtualSwitch.ConfigSpec.md#numStandalonePorts">numStandalonePorts</a>).   </p>   <p>   The <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md">DVPortgroupConfigInfo</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#numPorts">numPorts</a>   property is the total number of ports for a distributed virtual switch.   This total includes the ports generated by the static and dynamic portgroups   and the standalone ports.   </p>   </li><br />   <li>If you have created additional uplink portgroups, use the   <a href="vim.DistributedVirtualSwitch.md#reconfigure">ReconfigureDvs_Task</a> method   to add the portgroup(s) to the   <a href="vim.DistributedVirtualSwitch.ConfigSpec.md">DVSConfigSpec</a>.<a href="vim.DistributedVirtualSwitch.ConfigSpec.md#uplinkPortgroup">uplinkPortgroup</a>   array.   </li><br />   <li>Retrieve physical NIC device names from the host   (<a href="vim.HostSystem.md">HostSystem</a>.<a href="vim.HostSystem.md#config">config</a>.<a href="vim.host.ConfigInfo.md#network">network</a>.<a href="vim.host.NetworkInfo.md#pnic">pnic</a>[].<a href="vim.host.PhysicalNic.md#device">device</a>).</li><br />   <li>Add host member(s) to the distributed virtual switch. To configure host members:   <br /><br />   <ul>   <li>Specify hosts   (<a href="vim.DistributedVirtualSwitch.ConfigSpec.md">DVSConfigSpec</a>.<a href="vim.DistributedVirtualSwitch.ConfigSpec.md#host">host</a>[]).</li><br />   <li>For each host, specify one or more physical NIC device names   to identify the pNIC(s) for the host proxy connection to the network   (<a href="vim.dvs.HostMember.ConfigSpec.md">DistributedVirtualSwitchHostMemberConfigSpec</a>.<a href="vim.dvs.HostMember.ConfigSpec.md#backing">backing</a>.<a href="vim.dvs.HostMember.PnicBacking.md#pnicSpec">pnicSpec</a>[].<a href="vim.dvs.HostMember.PnicSpec.md#pnicDevice">pnicDevice</a>)   </li><br />   <li>Use the   <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.<a href="vim.DistributedVirtualSwitch.md#reconfigure">ReconfigureDvs_Task</a>   method to update the switch configuration.   </li>   </ul>   <p>   When you add a host to a distributed virtual switch   (<a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>.<a href="vim.DistributedVirtualSwitch.md#config">config</a>.<a href="vim.DistributedVirtualSwitch.ConfigInfo.md#host">host</a>),   the host automatically creates a proxy switch. The proxy switch is removed automatically   when the host is removed from the distributed virtual switch.   </li><br />   <li>Connect hosts and virtual machines to the distributed virtual switch.   <p>   <table style="border:0">   <tr>   <td style="border:0">Host connection</td>   <td style="border:0">Specify port or portgroup connections in the host virtual NIC spec   (<a href="vim.host.VirtualNic.Specification.md">HostVirtualNicSpec</a>.<a href="vim.host.VirtualNic.Specification.md#distributedVirtualPort">distributedVirtualPort</a>   or <a href="vim.host.VirtualNic.Specification.md">HostVirtualNicSpec</a>.<a href="vim.host.VirtualNic.Specification.md#portgroup">portgroup</a>).</td>   </tr>   <tr>   <td style="border:0">Virtual machine connection</td>   <td style="border:0">Specify port or portgroup connections in the distributed virtual port backing   (<a href="vim.vm.device.VirtualEthernetCard.DistributedVirtualPortBackingInfo.md">VirtualEthernetCardDistributedVirtualPortBackingInfo</a>)   for the virtual Ethernet cards on the virtual machine   (<a href="vim.vm.device.VirtualEthernetCard.md">VirtualEthernetCard</a>.<a href="vim.vm.device.VirtualDevice.md#backing">backing</a>).</td>   </tr>   </table>   </li>   </ol>   <h3>Backup, Rollback, and Query Operations</h3>   <p>   If you are using a <a href="vim.dvs.VmwareDistributedVirtualSwitch.md">VmwareDistributedVirtualSwitch</a>,   you can perform backup and rollback operations on the switch   and its associated distributed virtual portgroups.   </p>   When you reconfigure a VMware distributed virtual switch   (<a href="vim.DistributedVirtualSwitch.md#reconfigure">ReconfigureDvs_Task</a>), the Server   saves the current switch configuration before applying the   configuration updates. The saved switch configuration includes   portgroup configuration data. The Server uses the saved switch   configuration as a checkpoint for rollback operations.   You can rollback the switch or portgroup configuration   to the saved configuration, or you can rollback to a backup   configuration (<a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>).   </p>   <ul>   <li>To backup the switch and portgroup configuration, use the   <a href="vim.dvs.DistributedVirtualSwitchManager.md">DistributedVirtualSwitchManager</a>.<a href="vim.dvs.DistributedVirtualSwitchManager.md#exportEntity">DVSManagerExportEntity_Task</a>   method. The export method produces a   <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a> object. The backup configuration   contains the switch and/or portgroups specified in the   <code>SelectionSet</code> parameter.   To backup the complete configuration you must select the   distributed virtual switch and all of its portgroups.  </li><br />   <li>To rollback the switch configuration, use the   <a href="vim.DistributedVirtualSwitch.md#rollback">DVSRollback_Task</a> method   to determine if the switch configuration has changed.   If it has changed, use the   <a href="vim.DistributedVirtualSwitch.md#reconfigure">ReconfigureDvs_Task</a>    method to complete the rollback operation.</li><br />   <li>To rollback the portgroup configuration, use the   <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.<a href="vim.dvs.DistributedVirtualPortgroup.md#rollback">DVPortgroupRollback_Task</a>   method to determine if the portgroup configuration   has changed. If it has changed, use the   <a href="vim.dvs.DistributedVirtualPortgroup.md#reconfigure">ReconfigureDVPortgroup_Task</a>   method to complete the rollback operation.</li><br />   </ul>   <p>   To perform query operations on a distributed virtual switch,   use the <a href="vim.dvs.DistributedVirtualSwitchManager.md">DistributedVirtualSwitchManager</a> methods.   </p>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='uuid'>uuid</a> | string | None | None | Generated UUID of the switch. Unique across vCenter Server   inventory and instances. |
| <a href='capability'>capability</a> | [vim.DistributedVirtualSwitch.Capability](vim.DistributedVirtualSwitch.Capability.md "vim.DistributedVirtualSwitch.Capability") | None | None | Capability of the switch. Capabilities are indicated at the port,  portgroup and switch levels, and for version-specific features.  When you retrieve this property from an ESXi host,  <a href="vim.DistributedVirtualSwitch.md#capability">capability</a>.<a href="vim.DistributedVirtualSwitch.Capability.md#dvsOperationSupported">dvsOperationSupported</a>  should always be set to false. |
| <a href='summary'>summary</a> | [vim.DistributedVirtualSwitch.Summary](vim.DistributedVirtualSwitch.Summary.md "vim.DistributedVirtualSwitch.Summary") | None | None | Summary of the switch. |
| <a href='config'>config</a> | [vim.DistributedVirtualSwitch.ConfigInfo](vim.DistributedVirtualSwitch.ConfigInfo.md "vim.DistributedVirtualSwitch.ConfigInfo") | None | None | Switch configuration data. |
| <a href='networkResourcePool'>networkResourcePool</a> | [vim.dvs.NetworkResourcePool](vim.dvs.NetworkResourcePool.md "vim.dvs.NetworkResourcePool") | true | None | Network resource pool information for the switch. |
| <a href='portgroup'>portgroup</a> | [vim.dvs.DistributedVirtualPortgroup](vim.dvs.DistributedVirtualPortgroup.md "vim.dvs.DistributedVirtualPortgroup") | true | None | Portgroups that are defined on the switch. |
| <a href='runtime'>runtime</a> | [vim.DistributedVirtualSwitch.RuntimeInfo](vim.DistributedVirtualSwitch.RuntimeInfo.md "vim.DistributedVirtualSwitch.RuntimeInfo") | true | None | Runtime information of the distributed virtual switch. |


FetchDVPortKeys([criteria](vim.dvs.PortCriteria.md "vim.dvs.PortCriteria"))
---------------------------------------------------------------------------

| service name | FetchDVPortKeys |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




FetchDVPorts([criteria](vim.dvs.PortCriteria.md "vim.dvs.PortCriteria"))
------------------------------------------------------------------------

| service name | FetchDVPorts |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




QueryUsedVlanIdInDvs()
----------------------

| service name | QueryUsedVlanIdInDvs |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type | None |
### Faults
| fault | description |
|:------|:------------|




ReconfigureDvs([spec](vim.DistributedVirtualSwitch.ConfigSpec.md "vim.DistributedVirtualSwitch.ConfigSpec"))
------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.VspanDestPortConflict](vim.fault.VspanDestPortConflict.md "vim.fault.VspanDestPortConflict"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.VspanPromiscuousPortNotSupported](vim.fault.VspanPromiscuousPortNotSupported.md "vim.fault.VspanPromiscuousPortNotSupported"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.ResourceNotAvailable](vim.fault.ResourceNotAvailable.md "vim.fault.ResourceNotAvailable"), [vim.fault.VspanSameSessionPortConflict](vim.fault.VspanSameSessionPortConflict.md "vim.fault.VspanSameSessionPortConflict"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.LimitExceeded](vim.fault.LimitExceeded.md "vim.fault.LimitExceeded"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.VspanPortConflict](vim.fault.VspanPortConflict.md "vim.fault.VspanPortConflict"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | ReconfigureDvs |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | vim.fault.ConcurrentAccess |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | vim.fault.DuplicateName |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | vim.fault.InvalidName |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | vim.fault.AlreadyExists |
| [vim.fault.LimitExceeded](vim.fault.LimitExceeded.md "vim.fault.LimitExceeded") | vim.fault.LimitExceeded |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | vim.fault.ResourceInUse |
| [vim.fault.ResourceNotAvailable](vim.fault.ResourceNotAvailable.md "vim.fault.ResourceNotAvailable") | If there is no port available in the portgroup |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if called directly on a host or if the spec                         includes settings for any vNetwork Distributed                         Switch feature that is not supported on this                         switch. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the hosts being added lack support for any of the                           overlay classes of the switch's overlay instances. |
| [vim.fault.VspanPortConflict](vim.fault.VspanPortConflict.md "vim.fault.VspanPortConflict") | if dvPort is used as both the transmitted source and destination ports in Distributed Port Mirroring sessions. |
| [vim.fault.VspanPromiscuousPortNotSupported](vim.fault.VspanPromiscuousPortNotSupported.md "vim.fault.VspanPromiscuousPortNotSupported") | if a promiscuous port is used as transmitted source or destination in the Distributed Port Mirroring sessions. |
| [vim.fault.VspanSameSessionPortConflict](vim.fault.VspanSameSessionPortConflict.md "vim.fault.VspanSameSessionPortConflict") | if a dvPort is used as both the source and destination in the same Distributed Port Mirroring session. |
| [vim.fault.VspanDestPortConflict](vim.fault.VspanDestPortConflict.md "vim.fault.VspanDestPortConflict") | if a dvPort is used as desination ports in multiple Distributed Port Mirroring sessions. |




PerformDvsProductSpecOperation([operation](#string "string"), [productSpec](vim.dvs.ProductSpec.md "vim.dvs.ProductSpec"))
--------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | PerformDvsProductSpecOperation |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.Modify |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | vim.fault.TaskInProgress |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




MergeDvs([dvs](vim.DistributedVirtualSwitch.md "vim.DistributedVirtualSwitch"))
-------------------------------------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidHostState](vim.fault.InvalidHostState.md "vim.fault.InvalidHostState"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
### Deprecated
as of vSphere API 5.5

| service name | MergeDvs |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.Modify |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | If failed to delete the source switch |
| [vim.fault.InvalidHostState](vim.fault.InvalidHostState.md "vim.fault.InvalidHostState") | vim.fault.InvalidHostState |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




AddDVPortgroup([spec](vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md "vim.dvs.DistributedVirtualPortgroup.ConfigSpec"))
--------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | AddDVPortgroup |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | DVPortgroup.Create |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | vim.fault.DuplicateName |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | vim.fault.InvalidName |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




MoveDVPort([portKey](#string "string"), [destinationPortgroupKey](#string "string"))
------------------------------------------------------------------------------------
 raises [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | MoveDVPort |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.Modify |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | vim.fault.ConcurrentAccess |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




UpdateDvsCapability([capability](vim.DistributedVirtualSwitch.Capability.md "vim.DistributedVirtualSwitch.Capability"))
-----------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateDvsCapability |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.Modify |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host or if the switch                         implementation doesn't support this API. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




ReconfigureDVPort([port](vim.dvs.DistributedVirtualPort.ConfigSpec.md "vim.dvs.DistributedVirtualPort.ConfigSpec"))
-------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
| service name | ReconfigureDVPort |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.PortConfig |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | vim.fault.ResourceInUse |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | vim.fault.ConcurrentAccess |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If called directly on a host or if the switch                         implementation doesn't support this API or if the spec                         includes settings for any vSphere Distributed Switch                         feature that is not supported on this switch. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the array have different elements for the                         same port. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




RefreshDVPortState([portKeys](#string "string"))
------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RefreshDVPortState |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |




RectifyDvsHost([hosts](vim.HostSystem.md "vim.HostSystem"))
-----------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
### Deprecated
as of vSphere API 5.0.   Use   <a href="vim.dvs.DistributedVirtualSwitchManager.md">DistributedVirtualSwitchManager</a>.<a href="vim.dvs.DistributedVirtualSwitchManager.md#rectifyHost">RectifyDvsOnHost_Task</a> instead.

| service name | RectifyDvsHost |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |




UpdateNetworkResourcePool([configSpec](vim.dvs.NetworkResourcePool.ConfigSpec.md "vim.dvs.NetworkResourcePool.ConfigSpec"))
---------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
| service name | UpdateNetworkResourcePool |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.ResourceManagement |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the resource pool does not exist on the dvs. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name of the resource pool is invalid. |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | if a network resource pool is modified by           two or more clients at the same time. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if network I/O control is not supported on           the vSphere Distributed Switch. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




AddNetworkResourcePool([configSpec](vim.dvs.NetworkResourcePool.ConfigSpec.md "vim.dvs.NetworkResourcePool.ConfigSpec"))
------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | AddNetworkResourcePool |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.ResourceManagement |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | vim.fault.InvalidName |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if network I/O control is not supported on           the vSphere Distributed Switch. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




RemoveNetworkResourcePool([key](#string "string"))
--------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault")

---
| service name | RemoveNetworkResourcePool |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.ResourceManagement |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the resource pool does not exist on the dvs. |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if the name of the resource pool is invalid. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | If network resource pool is associated with a network entity |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if network I/O control is not supported on           the vSphere Distributed Switch. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




EnableNetworkResourceManagement()
---------------------------------
 raises [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | EnableNetworkResourceManagement |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.ResourceManagement |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if the enabling/disabling fails. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if network I/O control is not supported on           the vSphere Distributed Switch. |
| [vim.fault.DvsNotAuthorized](vim.fault.DvsNotAuthorized.md "vim.fault.DvsNotAuthorized") | if login-session's extension key does not match           the switch's configured           <a href="vim.DistributedVirtualSwitch.ConfigInfo.md#extensionKey">extensionKey</a>. |




DVSRollback([entityBackup](vim.dvs.EntityBackup.Config.md "vim.dvs.EntityBackup.Config"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.RollbackFailure](vim.fault.RollbackFailure.md "vim.fault.RollbackFailure")

---
| service name | DVSRollback |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails. |
| [vim.fault.RollbackFailure](vim.fault.RollbackFailure.md "vim.fault.RollbackFailure") | if there is no configuration specified in entityBackup and           the previous configuration does not exist either. |




CreateDVPortgroup([spec](vim.dvs.DistributedVirtualPortgroup.ConfigSpec.md "vim.dvs.DistributedVirtualPortgroup.ConfigSpec"))
-----------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName"), [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | CreateDVPortgroup |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | DVPortgroup.Create |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | if a portgroup with the same name already exists |
| [vim.fault.InvalidName](vim.fault.InvalidName.md "vim.fault.InvalidName") | if name of the portgroup is invalid |




UpdateDVSHealthCheckConfig([healthCheckConfig](vim.DistributedVirtualSwitch.HealthCheckConfig.md "vim.DistributedVirtualSwitch.HealthCheckConfig"))
---------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateDVSHealthCheckConfig |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | DVSwitch.Modify |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DvsFault](vim.fault.DvsFault.md "vim.fault.DvsFault") | if operation fails on any host or if there are other update failures. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if health check is not supported on the switch. |




LookupDvPortGroup([portgroupKey](#string "string"))
---------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | LookupDvPortGroup |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If the portgroup for the specified key is not found. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If the operation is not supported. |




