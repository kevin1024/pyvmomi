vSphere API enumerated types
============================


<a name='vim.action.Action.ActionParameter'>ActionParameter</a> - vim.action.Action
===================================================================================
These constant strings can be used as parameters in user-specified   email subject and body templates as well as in scripts. The action processor    in VirtualCenter substitutes the run-time values for the parameters.     For example, an email subject provided by the client could be the string:   <tt>"Alarm - {alarmName} Description:\n{eventDescription}"</tt>.     Or a script action provided could be: <tt>"myScript {alarmName}"</tt>
| name | description |
|:-----|:------------|
| targetName | The name of the entity where the alarm is triggered. |
| alarmName | The name of the triggering alarm. |
| oldStatus | The status prior to the alarm being triggered. |
| newStatus | The status after the alarm is triggered. |
| triggeringSummary | A summary of information involved in triggering the alarm. |
| declaringSummary | A summary of declarations made during the triggering of the alarm. |
| eventDescription | The event description. |
| target | The object of the entity where the alarm is assocaited. |
| alarm | The object of the triggering alarm. |


<a name='vim.cluster.Action.ActionType'>ActionType</a> - vim.cluster.Action
===========================================================================
Pre-defined constants for possible action types. Virtual Center   uses this information to coordinate with the clients.
| name | description |
|:-----|:------------|
| MigrationV1 | Migration action type |
| VmPowerV1 | Virtual machine power action type |
| HostPowerV1 | Host power action type |
| HostMaintenanceV1 | Host entering maintenance mode action type |
| StorageMigrationV1 | Storage migration action type |
| StoragePlacementV1 | Initial placement action for a virtual machine or a virtual disk |


<a name='vim.fault.AffinityConfigured.Affinity'>AffinityType</a> - vim.fault.AffinityConfigured
===============================================================================================
Types of affinities.
| name | description |
|:-----|:------------|
| memory | memory |
| cpu | cpu |


<a name='vim.fault.AgentInstallFailed.Reason'>AgentInstallFailedReason</a> - vim.fault.AgentInstallFailed
=========================================================================================================
| name | description |
|:-----|:------------|
| NotEnoughSpaceOnDevice | There is not enough storage space on the host to install the agent. |
| PrepareToUpgradeFailed | Failed to initialize the upgrade directory on the host. |
| AgentNotRunning | The agent was installed but is not running. |
| AgentNotReachable | The agent was installed but did not respond to requests. |
| InstallTimedout | The agent install took too long. |
| SignatureVerificationFailed | The signature verification for the installer failed. |
| AgentUploadFailed | Failed to upload the agent installer. |
| AgentUploadTimedout | The agent upload took too long. |
| UnknownInstallerError | The agent installer failed for an unknown reason. |


<a name='vim.option.ArrayUpdateSpec.Operation'>ArrayUpdateOperation</a> - vim.option.ArrayUpdateSpec
====================================================================================================
This list specifies the type of operation being performed on the array.
| name | description |
|:-----|:------------|
| add | indicates an addition to the array. |
| remove | indicates the removal of an element in the   array. In this case the key field must contain the key of the element   to be removed. |
| edit | indicates changes to an element in the array. |


<a name='vim.host.AutoStartManager.Action'>AutoStartAction</a> - vim.host.AutoStartManager
==========================================================================================
| name | description |
|:-----|:------------|
| none | No action is taken for this virtual machine. This virtual machine is   not a part of the auto-start sequence. This can be used for both auto-start   and auto-start settings. |
| systemDefault | The default system action is taken for this virtual machine when it is next in   the auto-start order. This can be used for both auto-start and auto-start   settings. |
| powerOn | This virtual machine is powered on when it is next in the auto-start order. |
| powerOff | This virtual machine is powered off when it is next in the auto-stop order.   This is the default stopAction. |
| guestShutdown | The guest operating system for a virtual machine is shut down when that   virtual machine in next in the auto-stop order. |
| suspend | This virtual machine is suspended when it is next in the auto-stop order. |


<a name='vim.host.AutoStartManager.AutoPowerInfo.WaitHeartbeatSetting'>AutoStartWaitHeartbeatSetting</a> - vim.host.AutoStartManager.AutoPowerInfo
==================================================================================================================================================
Determines if the virtual machine should start after receiving a heartbeat,   ignore heartbeats and start after the startDelay has elapsed, or follow the   system default before powering on. When a virtual machine is next in the start   order, the system either waits a specified period of time for a virtual   machine to power on or it waits until it receives a successful heartbeat from a   powered on virtual machine. By default, this is set to no.
| name | description |
|:-----|:------------|
| yes | The system waits until receiving a heartbeat before powering on the next   machine in the order. |
| no | The system does not wait to receive a heartbeat before powering on the next   machine in the order. This is the default setting. |
| systemDefault | The system uses the default value to determine whether or not to wait to   receive a heartbeat before powering on the next machine in the order. |


<a name='vim.fault.CannotMoveFaultToleranceVm.MoveType'>CannotMoveFaultToleranceVmMoveType</a> - vim.fault.CannotMoveFaultToleranceVm
=====================================================================================================================================
| name | description |
|:-----|:------------|
| resourcePool | Move out of the resouce pool |
| cluster | Move out of the cluster |


<a name='vim.fault.CannotPowerOffVmInCluster.Operation'>CannotPowerOffVmInClusterOperation</a> - vim.fault.CannotPowerOffVmInCluster
====================================================================================================================================
| name | description |
|:-----|:------------|
| suspend | suspend |
| powerOff | power off |
| guestShutdown | guest shutdown |
| guestSuspend | guest suspend |


<a name='vim.fault.CannotUseNetwork.Reason'>CannotUseNetworkReason</a> - vim.fault.CannotUseNetwork
===================================================================================================
| name | description |
|:-----|:------------|
| NetworkReservationNotSupported | Network does not support reservation |
| MismatchedNetworkPolicies | Source and destination networks do not have same security policies |
| MismatchedDvsVersionOrVendor | Source and destination DVS do not have same version or vendor |
| VMotionToUnsupportedNetworkType | VMotion to unsupported destination network type |


<a name='vim.vm.check.TestType'>CheckTestType</a> - None
========================================================
The types of tests which can requested by any of the methods in either   <a href="vim.vm.check.CompatibilityChecker.md">VirtualMachineCompatibilityChecker</a> or <a href="vim.vm.check.ProvisioningChecker.md">VirtualMachineProvisioningChecker</a>.
| name | description |
|:-----|:------------|
| sourceTests | Tests that examine only the configuration   of the virtual machine and its current host; the destination   resource pool and host or cluster are irrelevant. |
| hostTests | Tests that examine both the virtual   machine and the destination host or cluster; the destination   resource pool is irrelevant. This set excludes tests that fall   into the datastoreTests group. |
| resourcePoolTests | Tests that check that the destination resource   pool can support the virtual machine if it is powered on. The   destination host or cluster is relevant because it will affect the   amount of overhead memory required to run the virtual machine. |
| datastoreTests | Tests that check that the   destination host or cluster can see the datastores where the virtual   machine's virtual disks are going to be located. The destination   resource pool is irrelevant. |
| networkTests | Tests that check that the   destination host or cluster can see the networks that the virtual   machine's virtual nic devices are going to be connected. |


<a name='vim.cluster.DasAamNodeState.DasState'>ClusterDasAamNodeStateDasState</a> - vim.cluster.DasAamNodeState
===============================================================================================================
The <a href="vim.cluster.DasAamNodeState.DasState.md">ClusterDasAamNodeStateDasState</a> enumerated type defines  values for host HA configuration and runtime state properties  (<a href="vim.cluster.DasAamNodeState.md#configState">configState</a> and  <a href="vim.cluster.DasAamNodeState.md#runtimeState">runtimeState</a>).
| name | description |
|:-----|:------------|
| uninitialized | HA has never been enabled on the the host. |
| initialized | HA agents have been installed but are not running on the the host. |
| configuring | HA configuration is in progress. |
| unconfiguring | HA configuration is being removed. |
| running | HA agent is running on this host. |
| error | There is an error condition. This can represent a configuration   error or a host agent runtime error. |
| agentShutdown | The HA agent has been shut down. |
| nodeFailed | The host is not reachable. This can represent a host failure   or an isolated host. |


<a name='vim.cluster.DasConfigInfo.HBDatastoreCandidate'>ClusterDasConfigInfoHBDatastoreCandidate</a> - vim.cluster.DasConfigInfo
=================================================================================================================================
The policy to determine the candidates from which vCenter Server can  choose heartbeat datastores.
| name | description |
|:-----|:------------|
| userSelectedDs | vCenter Server chooses heartbeat datastores from the set specified  by the user (see <a href="vim.cluster.DasConfigInfo.md#heartbeatDatastore">heartbeatDatastore</a>). More specifically,  datastores not included in the set will not be chosen. Note that if  <a href="vim.cluster.DasConfigInfo.md#heartbeatDatastore">heartbeatDatastore</a> is empty, datastore heartbeating will  be disabled for HA. |
| allFeasibleDs | vCenter Server chooses heartbeat datastores from all the feasible ones,  i.e., the datastores that are accessible to more than one host in  the cluster. The choice will be made without giving preference to those  specified by the user (see <a href="vim.cluster.DasConfigInfo.md#heartbeatDatastore">heartbeatDatastore</a>). |
| allFeasibleDsWithUserPreference | vCenter Server chooses heartbeat datastores from all the feasible ones  while giving preference to those specified by the user (see <a href="vim.cluster.DasConfigInfo.md#heartbeatDatastore">heartbeatDatastore</a>).  More specifically, the datastores not included in <a href="vim.cluster.DasConfigInfo.md#heartbeatDatastore">heartbeatDatastore</a> will be  chosen if and only if the specified ones are not sufficient. |


<a name='vim.cluster.DasConfigInfo.ServiceState'>ClusterDasConfigInfoServiceState</a> - vim.cluster.DasConfigInfo
=================================================================================================================
Possible states of an HA service. All services support the  disabled and enabled states.
| name | description |
|:-----|:------------|
| disabled | HA service is disabled. |
| enabled | HA service is enabled. |


<a name='vim.cluster.DasConfigInfo.VmMonitoringState'>ClusterDasConfigInfoVmMonitoringState</a> - vim.cluster.DasConfigInfo
===========================================================================================================================
The <a href="vim.cluster.DasConfigInfo.VmMonitoringState.md">ClusterDasConfigInfoVmMonitoringState</a> enum defines values that indicate  the state of Virtual Machine Health Monitoring. Health Monitoring  uses the vmTools (guest) and application agent heartbeat modules.  You can configure HA to respond to heartbeat failures of either one  or both modules. You can also disable the HA response to heartbeat failures.  <ul>  <li>  To set the cluster default for health monitoring, use the  ClusterConfigSpecEx.dasConfig.<a href="vim.cluster.DasConfigInfo.md#vmMonitoring">vmMonitoring</a> property.  </li>  <li>  To set health monitoring for a virtual machine, use the  ClusterConfigSpecEx.dasVmConfigSpec.info.dasSettings.<a href="vim.cluster.DasVmSettings.md#vmToolsMonitoringSettings">vmToolsMonitoringSettings</a> property.  </li>  <li>  To retrieve the current state of health monitoring (cluster setting), use the  ClusterConfigInfoEx.dasConfig.<a href="vim.cluster.DasConfigInfo.md#vmMonitoring">vmMonitoring</a>  property.  </li>  <li>  To retrieve the current state of health monitoring for a virtual machine, use the  ClusterConfigInfoEx.dasVmConfig[].dasSettings.vmToolsMonitoringSettings.<a href="vim.cluster.VmToolsMonitoringSettings.md#vmMonitoring">vmMonitoring</a>  property.  </li>  </ul>
| name | description |
|:-----|:------------|
| vmMonitoringDisabled | Virtual machine health monitoring is disabled. In this state,  HA response to guest and application heartbeat failures are disabled. |
| vmMonitoringOnly | HA response to guest heartbeat failure is enabled.  To retrieve the guest heartbeat status, use the  <a href="vim.VirtualMachine.md">VirtualMachine</a>.<a href="vim.VirtualMachine.md#guestHeartbeatStatus">guestHeartbeatStatus</a>  property. |
| vmAndAppMonitoring | HA response to both guest and application heartbeat failure is enabled.  <ul>  <li>To retrieve the guest heartbeat status, use the  <a href="vim.VirtualMachine.md">VirtualMachine</a>.<a href="vim.VirtualMachine.md#guestHeartbeatStatus">guestHeartbeatStatus</a>  property.</li>  <li>To retrieve the application heartbeat status, use the  <a href="vim.vm.GuestInfo.md">GuestInfo</a>.<a href="vim.vm.GuestInfo.md#appHeartbeatStatus">appHeartbeatStatus</a>  property.</li>  </ul> |


<a name='vim.cluster.DasFdmAvailabilityState'>ClusterDasFdmAvailabilityState</a> - None
=======================================================================================
The <a href="vim.cluster.DasFdmAvailabilityState.md">ClusterDasFdmAvailabilityState</a> enumeration describes the   availability states of hosts in a vSphere HA cluster. In the HA   architecture, a agent called the Fault Domain Manager runs on   each active host. These agents elect a master and the others become   its slaves. The availability state assigned to a given host is   determined from information reported by the Fault Domain Manager   running on the host, by a Fault Domain Manager that has been elected   master, and by vCenter Server. See <a href="vim.cluster.DasFdmHostState.md">ClusterDasFdmHostState</a>   for more information about the vSphere HA architecture.
| name | description |
|:-----|:------------|
| uninitialized | The Fault Domain Manager for the host has not yet been   initialized. Hence the host is not part of a vSphere HA   fault domain. This state is reported by vCenter Server or   by the host itself. |
| election | The Fault Domain Manager on the host has been initialized and   the host is either waiting to join the existing master or   is participating in an election for a new master. This state   is reported by vCenter Server or by the host itself. |
| master | The Fault Domain Manager on the host has been elected a  master. This state is reported by the the host itself. |
| connectedToMaster | The normal operating state for a slave host. In this state,   the host is exchanging heartbeats with a master over   the management network, and is thus connected to it. If   there is a management network partition, the slave will be   in this state only if it is in the same partition as the master.   This state is reported by the master of a slave host. |
| networkPartitionedFromMaster | A slave host is alive and has management network connectivity, but   the management network has been partitioned. This state is reported   by masters that are in a partition other than the one containing the   slave host; the master in the slave's partition will report the slave state   as <a href="vim.cluster.DasFdmAvailabilityState.md#connectedToMaster">connectedToMaster</a>. |
| networkIsolated | A host is alive but is isolated from the management network.   See <a href="vim.cluster.DasVmSettings.IsolationResponse.md">ClusterDasVmSettingsIsolationResponse</a> for the criteria   used to determine whether a host is isolated. |
| hostDown | The slave host appears to be down. This state is reported by the   master of a slave host. |
| initializationError | An error occurred when initilizating the Fault Domain Manager   on a host due to a problem with installing the   agent or configuring it. This condition can often be cleared by   reconfiguring HA for the host. This state is reported by vCenter   Server. |
| uninitializationError | An error occurred when unconfiguring the Fault Domain Manager   running on a host. In order to clear this condition the host might   need to be reconnected to the cluster and reconfigured first.   This state is reported by vCenter   Server. |
| fdmUnreachable | The Fault Domain Manager (FDM) on the host cannot be reached. This   state is reported in two unlikley situations.   <ul>   <li> First, it is reported by   a master if the host responds to ICMP pings sent by the master over the   management network but the FDM on the host cannot be reached by the master.   This situation will occur if the FDM is unable to run or exit the   uninitialized state.   <li> Second, it is reported by vCenter Server if it cannot connect to a   master nor the FDM for the host. This situation would occur if all hosts   in the cluster failed but vCenter Server is still running. It may also   occur if all FDMs are unable to run or exit the uninitialized state.   </ul> |


<a name='vim.cluster.DasVmSettings.IsolationResponse'>ClusterDasVmSettingsIsolationResponse</a> - vim.cluster.DasVmSettings
===========================================================================================================================
The <a href="vim.cluster.DasVmSettings.IsolationResponse.md">ClusterDasVmSettingsIsolationResponse</a> enum defines   values that indicate whether or not the virtual machine should be   powered off if a host determines that it is isolated from   the rest of the cluster.  <p>  Host network isolation occurs when a host is still running  but it can no longer communicate with other hosts in the cluster  and it cannot ping the configured isolation address(es).  When the HA agent on a host loses contact with the other hosts,  it will ping the isolation addresses. If the pings fail, the host  will declare itself isolated.  <p>  Once the HA agent declares the host isolated, it will  initiate the isolation response workflow after a 30 second delay. You can use  the FDM advanced option fdm.isolationPolicyDelaySec to increase the delay.  For each virtual machine, the HA agent attempts to determine if a master is  responsible for restarting the virtual machine. If it cannot make the determination,  or there is a master that is responsible, the agent will apply the configured  isolation response. This workflow will continue until the configuration policy,  has been applied to all virtual machines, the agent reconnects to another HA agent  in the cluster, or the isolation address pings start succeeding. If there is a  master agent in the cluster, it will attempt to restart the virtual machines  that were powered off during isolation.  <p>  By default, the isolated host leaves its virtual machines powered on.  You can override the isolation response default with a cluster-wide setting  (<a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>)  or a virtual machine setting  (<a href="vim.cluster.DasVmSettings.md#isolationResponse">isolationResponse</a>).  <ul>  <li>All isolation response values are valid for the  <a href="vim.cluster.DasVmSettings.md#isolationResponse">isolationResponse</a>  property specified in a single virtual machine HA configuration.</li>  <li>All values except for <code>clusterIsolationResponse</code> are valid  for the cluster-wide default HA configuration for virtual machines  (<a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>).  </ul>   <p>   If you ensure that your network infrastructure is sufficiently redundant   and that at least one network path is available at all times, host network   isolation should be a rare occurrence.
| name | description |
|:-----|:------------|
| none | Do not power off the virtual machine in the event of a host network isolation. |
| powerOff | Power off the virtual machine in the event of a host network isolation. |
| shutdown | Shut down the virtual machine guest operating system   in the event of a host network isolation.   If the guest operating system fails to shutdown within five minutes,   HA will initiate a forced power off.   <p>   When you use the shutdown isolation response, failover can take   longer (compared to the   <a href="vim.cluster.DasVmSettings.IsolationResponse.md#powerOff">powerOff</a>   response) because the virtual machine cannot fail over until it is shutdown. |
| clusterIsolationResponse | Use the default isolation reponse defined for the cluster   that contains this virtual machine. |


<a name='vim.cluster.DasVmSettings.RestartPriority'>ClusterDasVmSettingsRestartPriority</a> - vim.cluster.DasVmSettings
=======================================================================================================================
The <a href="vim.cluster.DasVmSettings.RestartPriority.md">ClusterDasVmSettingsRestartPriority</a> enum   defines virtual machine restart priority values to resolve   resource contention.   The priority determines the preference that HA gives   to a virtual machine if sufficient capacity is not available   to power on all failed virtual machines. For example, high priority   virtual machines on a host get preference over low priority   virtual machines.   <p>   All priority values are valid for the restart priority   specified in a single virtual machine HA configuration   (<a href="vim.cluster.DasVmConfigInfo.md#dasSettings">dasSettings</a>).   All values except for <code>clusterRestartPriority</code>   are valid for the cluster-wide default HA configuration   for virtual machines (<a href="vim.cluster.DasConfigInfo.md#defaultVmSettings">defaultVmSettings</a>).
| name | description |
|:-----|:------------|
| disabled | vSphere HA is disabled for this virtual machine. |
| low | Virtual machines with this priority have a lower chance of powering on after a   failure if there is insufficient capacity on hosts to meet all virtual machine   needs. |
| medium | Virtual machines with this priority have an intermediate chance of powering    on after a failure if there is insufficient capacity on hosts to meet all    virtual machine needs. |
| high | Virtual machines with this priority have a higher chance of powering on after a    failure if there is insufficient capacity on hosts to meet all virtual machine    needs. |
| clusterRestartPriority | Virtual machines with this priority use the default restart   priority defined for the cluster that contains this virtual machine. |


<a name='vim.cluster.PowerOnVmOption'>ClusterPowerOnVmOption</a> - None
=======================================================================
Defines the options for a Datacenter::powerOnVm() invocation.
| name | description |
|:-----|:------------|
| OverrideAutomationLevel | Override the DRS automation level.         Value type: <a href="vim.cluster.DrsConfigInfo.DrsBehavior.md">DrsBehavior</a>         Default value: current behavior |
| ReserveResources | Reserve resources for the powering-on VMs throughout the         power-on session. When this option is set to true, the server         will return at most one recommended host per manual VM, and         the VM's reservations are held on the recommended host until         the VM is actually powered on (either by applying the         recommendation or by a power-on request on the VM), or until         the recommendation is cancelled, or until the recommendation         expires. The expiration time is currently set to 10         minutes. This option does not have an effect on automatic VMs         since their recommendations are executed immediately. This         option is effective on DRS clusters only.           Value type: boolean         Default value: false |


<a name='vim.profile.cluster.ClusterProfile.ServiceType'>ClusterProfileServiceType</a> - vim.profile.cluster.ClusterProfile
===========================================================================================================================
Type of services for which Profile can be requested for
| name | description |
|:-----|:------------|
| DRS | Distributed Resource Scheduling |
| HA | High Availability |
| DPM | Distributed Power Management |
| FT | Fault tolerance |


<a name='vim.profile.ComplianceResult.Status'>ComplianceResultStatus</a> - vim.profile.ComplianceResult
=======================================================================================================
| name | description |
|:-----|:------------|
| compliant | Entity is in Compliance |
| nonCompliant | Entity is out of Compliance |
| unknown | Compliance status of the entity is not known |


<a name='vim.ComputeResource.HostSPBMLicenseInfo.HostSPBMLicenseState'>ComputeResourceHostSPBMLicenseInfoHostSPBMLicenseState</a> - vim.ComputeResource.HostSPBMLicenseInfo
===========================================================================================================================================================================
The SPBM(Storage Policy Based Management) license state for a host
| name | description |
|:-----|:------------|
| licensed | The host is licensed |
| unlicensed | The host is not licensed |
| unknown | The host license information is unknown, this could happen if the  host is not in a available state |


<a name='vim.ConfigSpecOperation'>ConfigSpecOperation</a> - None
================================================================
Config spec operation type.
| name | description |
|:-----|:------------|
| add | Indicates the addition of an element to the configuration. |
| edit | Indicates the change of an element in the configuration. |
| remove | Indicates the removal of an element in the configuration. |


<a name='vim.vm.customization.LicenseFilePrintData.AutoMode'>CustomizationLicenseDataMode</a> - vim.vm.customization.LicenseFilePrintData
=========================================================================================================================================
Enumeration of AutoMode values.
| name | description |
|:-----|:------------|
| perServer | Indicates that client access licenses have been purchased for the server,   allowing a certain number of concurrent connections to the VirtualCenter   server. |
| perSeat | Indicates that a client access license has been purchased for each computer   that accesses the VirtualCenter server. |


<a name='vim.vm.customization.IPSettings.NetBIOSMode'>CustomizationNetBIOSMode</a> - vim.vm.customization.IPSettings
====================================================================================================================
NetBIOS setting for Windows.
| name | description |
|:-----|:------------|
| enableNetBIOSViaDhcp | DHCP server decides whether or not to use NetBIOS. |
| enableNetBIOS | Always use NetBIOS. |
| disableNetBIOS | Never use NetBIOS. |


<a name='vim.vm.customization.WinOptions.SysprepRebootOption'>CustomizationSysprepRebootOption</a> - vim.vm.customization.WinOptions
====================================================================================================================================
A enum constant specifying what should be done to the guest vm after running  sysprep.
| name | description |
|:-----|:------------|
| reboot | Reboot the machine after running sysprep. This will cause values  specified in the sysprep.inf to be applied immediately. |
| noreboot | Take no action. Leave the guest os running after running sysprep. This  option can be used to look at values for debugging purposes after  running sysprep. |
| shutdown | Shutdown the machine after running sysprep. This puts the vm in a  sealed state. |


<a name='vim.dvs.DistributedVirtualPort.RuntimeInfo.VmDirectPathGen2InactiveReasonNetwork'>DVPortStatusVmDirectPathGen2InactiveReasonNetwork</a> - vim.dvs.DistributedVirtualPort.RuntimeInfo
=============================================================================================================================================================================================
Set of possible values for  <a href="vim.dvs.DistributedVirtualPort.RuntimeInfo.md">DVPortStatus</a>.<a href="vim.dvs.DistributedVirtualPort.RuntimeInfo.md#vmDirectPathGen2InactiveReasonNetwork">vmDirectPathGen2InactiveReasonNetwork</a>.
| name | description |
|:-----|:------------|
| portNptIncompatibleDvs | The switch for which this port is defined does not support VMDirectPath Gen 2.   See  <a href="vim.DistributedVirtualSwitch.FeatureCapability.md">DVSFeatureCapability</a>.<a href="vim.DistributedVirtualSwitch.FeatureCapability.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a>. |
| portNptNoCompatibleNics | None of the physical NICs used as uplinks for this port support   VMDirectPath Gen 2.<br>See <a href="vim.host.PhysicalNic.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a><br> |
| portNptNoVirtualFunctionsAvailable | At least some of the physical NICs used as uplinks for this port   support VMDirectPath Gen 2, but all available network-passthrough   resources are in use by other ports. |
| portNptDisabledForPort | VMDirectPath Gen 2 has been explicitly disabled for this port. |


<a name='vim.dvs.DistributedVirtualPort.RuntimeInfo.VmDirectPathGen2InactiveReasonOther'>DVPortStatusVmDirectPathGen2InactiveReasonOther</a> - vim.dvs.DistributedVirtualPort.RuntimeInfo
=========================================================================================================================================================================================
Set of possible values for   <a href="vim.dvs.DistributedVirtualPort.RuntimeInfo.md">DVPortStatus</a>.<a href="vim.dvs.DistributedVirtualPort.RuntimeInfo.md#vmDirectPathGen2InactiveReasonOther">vmDirectPathGen2InactiveReasonOther</a>.
| name | description |
|:-----|:------------|
| portNptIncompatibleHost | The host for which this port is defined does not support VMDirectPath Gen 2.   See <a href="vim.host.Capability.md">HostCapability</a>.<a href="vim.host.Capability.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a> |
| portNptIncompatibleConnectee | Configuration or state of the port's connectee prevents   VMDirectPath Gen 2. See   <a href="vim.vm.DeviceRuntimeInfo.VirtualEthernetCardRuntimeState.md#vmDirectPathGen2InactiveReasonVm">vmDirectPathGen2InactiveReasonVm</a>   and/or   <a href="vim.vm.DeviceRuntimeInfo.VirtualEthernetCardRuntimeState.md#vmDirectPathGen2InactiveReasonExtended">vmDirectPathGen2InactiveReasonExtended</a>   in the appropriate element of the RuntimeInfo.device array of the   virtual machine connected to this port. |


<a name='vim.fault.DasConfigFault.DasConfigFaultReason'>DasConfigFaultDasConfigFaultReason</a> - vim.fault.DasConfigFault
=========================================================================================================================
| name | description |
|:-----|:------------|
| HostNetworkMisconfiguration | There is a problem with the host network configuration. |
| HostMisconfiguration | There is a problem with the host configuration. |
| InsufficientPrivileges | The privileges were insuffient for the operation. |
| NoPrimaryAgentAvailable | There was no running primary agent available to contact.    Check that your other hosts don't have HA errors |
| Other | The HA configuration failed for other reasons. |
| NoDatastoresConfigured | No datastores defined for this host |
| VSanNotSupportedOnHost | Host in vSAN cluster does not support vSAN. |


<a name='vim.cluster.DasVmConfigInfo.Priority'>DasVmPriority</a> - vim.cluster.DasVmConfigInfo
==============================================================================================
The priority of the virtual machine determines the preference   given to it if sufficient capacity is not available to power   on all failed virtual machines. For example, high priority   virtual machines on a host get preference over low priority   virtual machines.
| name | description |
|:-----|:------------|
| disabled | vSphere HA is disabled for this virtual machine. |
| low | Virtual machines with this priority have a lower chance of powering on after a   failure if there is insufficient capacity on hosts to meet all virtual machine   needs. |
| medium | Virtual machines with this priority have an intermediate chance of powering    on after a failure if there is insufficient capacity on hosts to meet all    virtual machine needs. |
| high | Virtual machines with this priority have a higher chance of powering on after a    failure if there is insufficient capacity on hosts to meet all virtual machine    needs. |


<a name='vim.Datastore.Accessible'>DatastoreAccessible</a> - vim.Datastore
==========================================================================
| name | description |
|:-----|:------------|
| True | Is accessible |
| False | Is not accessible |


<a name='vim.Datastore.Summary.MaintenanceModeState'>DatastoreSummaryMaintenanceModeState</a> - vim.Datastore.Summary
=====================================================================================================================
Defines the current maintenance mode state of the datastore.
| name | description |
|:-----|:------------|
| normal | Default state. |
| enteringMaintenance | Started entering maintenance mode, but not finished.  This could happen when waiting for user input or for  long-running vmotions to complete. |
| inMaintenance | Successfully entered maintenance mode. |


<a name='vim.scheduler.MonthlyByWeekdayTaskScheduler.DayOfWeek'>DayOfWeek</a> - vim.scheduler.MonthlyByWeekdayTaskScheduler
===========================================================================================================================
| name | description |
|:-----|:------------|
| sunday | sunday |
| monday | monday |
| tuesday | tuesday |
| wednesday | wednesday |
| thursday | thursday |
| friday | friday |
| saturday | saturday |


<a name='vim.fault.DeviceNotSupported.Reason'>DeviceNotSupportedReason</a> - vim.fault.DeviceNotSupported
=========================================================================================================
Reasons why a virtual device would not be supported on a host.
| name | description |
|:-----|:------------|
| host | The host does not support this virtual device at all. |
| guest | The device is supported by the host in general, but not for  the specific guest OS the virtual machine is using. |


<a name='vim.DiagnosticManager.LogDescriptor.Creator'>DiagnosticManagerLogCreator</a> - vim.DiagnosticManager.LogDescriptor
===========================================================================================================================
Pre-defined constants for possible creators of log files.
| name | description |
|:-----|:------------|
| vpxd | VirtualCenter service |
| vpxa | VirtualCenter agent |
| hostd | Host agent |
| serverd | Host server agent |
| install | Installation |
| vpxClient | Virtual infrastructure client |
| recordLog | System Record Log |


<a name='vim.DiagnosticManager.LogDescriptor.Format'>DiagnosticManagerLogFormat</a> - vim.DiagnosticManager.LogDescriptor
=========================================================================================================================
Constants for defined formats. For more information, see the comment for the    format property.
| name | description |
|:-----|:------------|
| plain | A standard ASCII-based line-based log file. |


<a name='vim.host.DiagnosticPartition.StorageType'>DiagnosticPartitionStorageType</a> - vim.host.DiagnosticPartition
====================================================================================================================
Type of partition indicating the type of storage on which the partition   resides.  If the diagnostic partition is local only, it will only need   one slot.  If the diagnostic partition is on shared storage, it could   be used by multiple hosts.  As a result, it will need multiple slots.
| name | description |
|:-----|:------------|
| directAttached | directAttached |
| networkAttached | networkAttached |


<a name='vim.host.DiagnosticPartition.DiagnosticType'>DiagnosticPartitionType</a> - vim.host.DiagnosticPartition
================================================================================================================
The type of diagnostic partition. Private diagnostic partition has one  slot, so can only be used by one host. Shared diagnostic parititon  needs multiple slots so to be usable by multiple hosts.
| name | description |
|:-----|:------------|
| singleHost | singleHost |
| multiHost | multiHost |


<a name='vim.fault.DisallowedChangeByService.DisallowedChange'>DisallowedChangeByServiceDisallowedChange</a> - vim.fault.DisallowedChangeByService
==================================================================================================================================================
The disallowed change type.
| name | description |
|:-----|:------------|
| hotExtendDisk | Online extend disk operation. |


<a name='vim.dvs.DistributedVirtualPortgroup.MetaTagName'>DistributedVirtualPortgroupMetaTagName</a> - vim.dvs.DistributedVirtualPortgroup
==========================================================================================================================================
The meta tag names recognizable in the   <a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#portNameFormat">portNameFormat</a> string.
| name | description |
|:-----|:------------|
| dvsName | This tag will be expanded to the name of the switch. |
| portgroupName | This tag will be expanded to the name of the portgroup. |
| portIndex | This tag will be expanded to the current index of the port. |


<a name='vim.dvs.DistributedVirtualPortgroup.PortgroupType'>DistributedVirtualPortgroupPortgroupType</a> - vim.dvs.DistributedVirtualPortgroup
==============================================================================================================================================
The <a href="vim.dvs.DistributedVirtualPortgroup.PortgroupType.md">DistributedVirtualPortgroupPortgroupType</a> enum defines  the distributed virtual portgroup types  (<a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.<a href="vim.dvs.DistributedVirtualPortgroup.md#config">config</a>.<a href="vim.dvs.DistributedVirtualPortgroup.ConfigInfo.md#type">type</a>). Early binding specifies a static set of ports that are created  when you create the distributed virtual portgroup. An ephemeral portgroup uses dynamic  ports that are created when you power on a virtual machine.
| name | description |
|:-----|:------------|
| earlyBinding | A free <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a> will be selected and assigned to   a <a href="vim.VirtualMachine.md">VirtualMachine</a> when the virtual machine is reconfigured to   connect to the portgroup. |
| lateBinding | <b>Deprecated</b> as of vSphere API 5.0. A free distributed virtual port   will be selected and assigned to a virtual machine when the virtual   machine is powered on. |
| ephemeral | A <a href="vim.dvs.DistributedVirtualPort.md">DistributedVirtualPort</a> will be created and assigned to a   <a href="vim.VirtualMachine.md">VirtualMachine</a> when the virtual machine is powered on, and will   be deleted when the virtual machine is powered off. An ephemeral portgroup has   no limit on the number of ports that can be a part of this portgroup.   In cases where the vCenter Server is unavailable the host can   create conflict ports in this portgroup to be used by a virtual machine   at power on. |


<a name='vim.DistributedVirtualSwitch.HostInfrastructureTrafficClass'>DistributedVirtualSwitchHostInfrastructureTrafficClass</a> - vim.DistributedVirtualSwitch
===============================================================================================================================================================
List of possible host infrastructure traffic classes
| name | description |
|:-----|:------------|
| management | Management Traffic |
| faultTolerance | Fault Tolerance (FT) Traffic |
| vmotion | vMotion Traffic |
| virtualMachine | Virtual Machine Traffic |
| iSCSI | iSCSI Traffic |
| nfs | NFS Traffic |
| hbr | vSphere Replication (VR) Traffic |
| vsan | vSphere Storage Area Network Traffic |


<a name='vim.dvs.HostMember.HostComponentState'>DistributedVirtualSwitchHostMemberHostComponentState</a> - vim.dvs.HostMember
=============================================================================================================================
Describes the state of the host proxy switch.
| name | description |
|:-----|:------------|
| up | The host proxy switch is up and running. |
| pending | The host proxy switch is waiting to be initialized. |
| outOfSync | The proxy switch configuration is not the same as the  distributed virtual switch configuration in the vCenter Server. |
| warning | The host requires attention. |
| disconnected | The host is disconnected or it is not responding. |
| down | The host proxy is down. |


<a name='vim.DistributedVirtualSwitch.NicTeamingPolicyMode'>DistributedVirtualSwitchNicTeamingPolicyMode</a> - vim.DistributedVirtualSwitch
===========================================================================================================================================
List of possible teaming modes supported by the vNetwork Distributed   Switch. The different policy modes define the way traffic is routed   through the different uplink ports in a team.
| name | description |
|:-----|:------------|
| loadbalance_ip | Routing based on IP hash |
| loadbalance_srcmac | Route based on source MAC hash |
| loadbalance_srcid | Route based on the source of the port ID |
| failover_explicit | Use explicit failover order |
| loadbalance_loadbased | Routing based by dynamically balancing traffic through the NICs   in a team. This is the recommended teaming policy when the   network I/O control feature is enabled for the vNetwork   Distributed Switch. |


<a name='vim.dvs.PortConnectee.ConnecteeType'>DistributedVirtualSwitchPortConnecteeConnecteeType</a> - vim.dvs.PortConnectee
============================================================================================================================
The connectee types.
| name | description |
|:-----|:------------|
| pnic | The port connects to a Physical NIC. |
| vmVnic | The port connects to a Virtual NIC in a Virtual Machine. |
| hostConsoleVnic | The port connects to a console Virtual NIC on a host. |
| hostVmkVnic | The port connects to a VMkernel Virtual NIC on a host. |


<a name='vim.DistributedVirtualSwitch.ProductSpecOperationType'>DistributedVirtualSwitchProductSpecOperationType</a> - vim.DistributedVirtualSwitch
===================================================================================================================================================
The product spec operation types.
| name | description |
|:-----|:------------|
| preInstall | Push the switch's host component of the specified product info to the   host members of the switch at a fixed location known by the host. |
| upgrade | Change the switch implementation to use the specified one. If the   property values in the specified product info are different from   those of the corresponding properties in the switch's product info,   a host component preinstall and switch upgrade will be performed. |
| notifyAvailableUpgrade | Set the product information for an available switch upgrade that   would be done by the switch implementation. This operation will post   a config issue on the switch to signal the availability of an upgrade.   This operation is applicable only in the case when switch policy   <a href="vim.DistributedVirtualSwitch.SwitchPolicy.md#autoUpgradeAllowed">autoUpgradeAllowed</a>   is set to false. |
| proceedWithUpgrade | If productSpec is set to be same as that in the   <a href="vim.event.DvsUpgradeAvailableEvent.md">DvsUpgradeAvailableEvent</a> configIssue, the switch   implementation will proceed with the upgrade. To reject or stop the   upgrade, leave the productSpec unset. If productSpec is set but does not   match that in <a href="vim.event.DvsUpgradeAvailableEvent.md">DvsUpgradeAvailableEvent</a> configIssue,   a fault will be raised.   This operation is applicable only in the case when switch policy   <a href="vim.DistributedVirtualSwitch.SwitchPolicy.md#autoUpgradeAllowed">autoUpgradeAllowed</a>   is set to false. |
| updateBundleInfo | Update the bundle URL and ID information. If other properties in   the specified product info differ from the   corresponding properties of the switch's product info, a fault will   be thrown. Updating the bundle ID will result in installing the new host   component identified by the bundle ID. |


<a name='vim.cluster.DpmConfigInfo.DpmBehavior'>DpmBehavior</a> - vim.cluster.DpmConfigInfo
===========================================================================================
| name | description |
|:-----|:------------|
| manual | Specifies that VirtualCenter should generate recommendations   for host power operations, but should not execute the   recommendations automatically. |
| automated | Specifies that VirtualCenter should generate recommendations   for host power operations, and should execute the   recommendations automatically. |


<a name='vim.cluster.DrsConfigInfo.DrsBehavior'>DrsBehavior</a> - vim.cluster.DrsConfigInfo
===========================================================================================
| name | description |
|:-----|:------------|
| manual | Specifies that VirtualCenter should generate recommendations for   virtual machine migration and for placement with a host,   but should not implement the recommendations automatically. |
| partiallyAutomated | Specifies that VirtualCenter should generate recommendations for   virtual machine migration and for placement with a host,   but should automatically implement only the placement at power on. |
| fullyAutomated | Specifies that VirtualCenter should automate both the migration   of virtual machines and their placement with a host at power on. |


<a name='vim.DrsStatsManager.InjectorWorkload.CorrelationState'>DrsInjectorWorkloadCorrelationState</a> - vim.DrsStatsManager.InjectorWorkload
==============================================================================================================================================
Correlation state as computed by storageRM  module on host.
| name | description |
|:-----|:------------|
| Correlated | Correlated |
| Uncorrelated | Uncorrelated |


<a name='vim.cluster.DrsRecommendation.ReasonCode'>DrsRecommendationReasonCode</a> - vim.cluster.DrsRecommendation
==================================================================================================================
List of defined migration reason codes:
| name | description |
|:-----|:------------|
| fairnessCpuAvg | Balance average CPU utilization. |
| fairnessMemAvg | Balance average memory utilization. |
| jointAffin | Fulfill affinity rule. |
| antiAffin | Fulfill anti-affinity rule. |
| hostMaint | Host entering maintenance mode. |


<a name='vim.dvs.DistributedVirtualPort.FilterOnFailure'>DvsFilterOnFailure</a> - vim.dvs.DistributedVirtualPort
================================================================================================================
Network Filter on Failure Type. It specifies whether all the   packets will be allowed or all the packets will be denied when   Filter fails to configure.
| name | description |
|:-----|:------------|
| failOpen | Allows all the packets when the Filter fails to configure. |
| failClosed | Denies all the packets when the Filter fails to configure. |


<a name='vim.dvs.TrafficRule.RuleDirectionType'>DvsNetworkRuleDirectionType</a> - vim.dvs.TrafficRule
=====================================================================================================
Network Traffic Rule direction types. It specifies whether rule    needs to be applied for packets which are incoming/outgoing or both.
| name | description |
|:-----|:------------|
| incomingPackets | This specifies that the network rule has to be applied only for     incoming packets. |
| outgoingPackets | This specifies that the network rule has to be applied only for     outgoing packets. |
| both | This specifies that the network rule has to be applied only for     both incoming and outgoing packets. |


<a name='vim.dvs.EntityBackup.ImportType'>EntityImportType</a> - vim.dvs.EntityBackup
=====================================================================================
The <a href="vim.dvs.EntityBackup.ImportType.md">EntityImportType</a> enum defines the import type for a  <a href="vim.dvs.DistributedVirtualSwitchManager.md">DistributedVirtualSwitchManager</a>.<a href="vim.dvs.DistributedVirtualSwitchManager.md#importEntity">DVSManagerImportEntity_Task</a>  operation.
| name | description |
|:-----|:------------|
| createEntityWithNewIdentifier | Create the entity with new identifiers. Specify the  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#name">name</a> and  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#container">container</a>  properties.  <p>  The Server ignores any value for the  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#key">key</a>  property. |
| createEntityWithOriginalIdentifier | Recreate the entities with the original identifiers of the entity from which backup was created.  The Server throws an exception if an entity with the same identifier already exists.  This option will also add the host members to the <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a> and will  try to get the virtual machine networking back with the same <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>.  Specify a <a href="vim.Folder.md">Folder</a> as the  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#container">container</a>  for <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#entityType">entityType</a>  "distributedVirtualSwitch".  <p>  The Server ignores any values for the  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#key">key</a> and  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#name">name</a>  properties. |
| applyToEntitySpecified | Apply the configuration specified in the  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#configBlob">configBlob</a>  property to the entity specified in the  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#entityType">entityType</a> and  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#key">key</a>  properties. If you specify  <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#name">name</a>,  the Server uses the specified name to rename the entity.  <p>  The Server ignores any value for the   <a href="vim.dvs.EntityBackup.Config.md">EntityBackupConfig</a>.<a href="vim.dvs.EntityBackup.Config.md#container">container</a>  property. |


<a name='vim.dvs.EntityBackup.EntityType'>EntityType</a> - vim.dvs.EntityBackup
===============================================================================
The <a href="vim.dvs.EntityBackup.EntityType.md">EntityType</a> enum identifies  the type of entity that was exported  (<a href="vim.dvs.DistributedVirtualSwitchManager.md#exportEntity">DVSManagerExportEntity_Task</a>).
| name | description |
|:-----|:------------|
| distributedVirtualSwitch | Indicates the exported entity is a <a href="vim.DistributedVirtualSwitch.md">DistributedVirtualSwitch</a>. |
| distributedVirtualPortgroup | Indicates the exported entity is a <a href="vim.dvs.DistributedVirtualPortgroup.md">DistributedVirtualPortgroup</a>. |


<a name='vim.alarm.EventAlarmExpression.ComparisonOperator'>EventAlarmExpressionComparisonOperator</a> - vim.alarm.EventAlarmExpression
=======================================================================================================================================
Basic Comparison operators
| name | description |
|:-----|:------------|
| equals | attribute equals specified value |
| notEqualTo | attribute does not equal specified value |
| startsWith | attribute starts with specified value |
| doesNotStartWith | attribute does not start with specified value |
| endsWith | attribute ends with specified value |
| doesNotEndWith | attribute does not end with specified value |


<a name='vim.event.EventDescription.EventCategory'>EventCategory</a> - vim.event.EventDescription
=================================================================================================
| name | description |
|:-----|:------------|
| info | Returns informational events. |
| warning | Returns warning events. |
| error | Returns error events. |
| user | Returns events pertaining to users. |


<a name='vim.event.Event.EventSeverity'>EventEventSeverity</a> - vim.event.Event
================================================================================
Severity level constants.
| name | description |
|:-----|:------------|
| error | Something that must be corrected |
| warning | Should be corrected, but the system can continue operating normally |
| info | An informational message |
| user | A user-related message |


<a name='vim.event.EventFilterSpec.RecursionOption'>EventFilterSpecRecursionOption</a> - vim.event.EventFilterSpec
==================================================================================================================
This option specifies how to select events based on child relationships   in the inventory hierarchy. If a managed entity has children, their events   can be retrieved with this filter option.
| name | description |
|:-----|:------------|
| self | Returns events that pertain only to the specified managed entity,   and not its children. |
| children | Returns events pertaining to child entities only. Excludes   events pertaining to the specified managed entity itself. |
| all | Returns events pertaining either to the specified managed entity   or to its child entities. |


<a name='vim.host.FibreChannelHba.PortType'>FibreChannelPortType</a> - vim.host.FibreChannelHba
===============================================================================================
The operating mode of the adapter.
| name | description |
|:-----|:------------|
| fabric | fabric |
| loop | loop |
| pointToPoint | pointToPoint |
| unknown | unknown |


<a name='vim.host.FileSystemMountInfo.VStorageSupportStatus'>FileSystemMountInfoVStorageSupportStatus</a> - vim.host.FileSystemMountInfo
========================================================================================================================================
Status of volume's support for vStorage hardware acceleration.   The ESX Server determines the status based on the capabilities   of the devices that support the file system volume.   When a host boots, the support status is unknown.   As the ESX host attempts hardware-accelerated operations,   it determines whether the storage device supports hardware   acceleration and sets the <a href="vim.host.FileSystemMountInfo.md#vStorageSupport">vStorageSupport</a>   property accordingly.
| name | description |
|:-----|:------------|
| vStorageSupported | Storage device supports hardware acceleration.  The ESX host will use the feature to offload certain  storage-related operations to the device. |
| vStorageUnsupported | Storage device does not support hardware acceleration.  The ESX host will handle all storage-related operations. |
| vStorageUnknown | Initial support status value. |


<a name='vim.fault.FtIssuesOnHost.HostSelectionType'>FtIssuesOnHostHostSelectionType</a> - vim.fault.FtIssuesOnHost
===================================================================================================================
HostSelectionType defines how the host was selected
| name | description |
|:-----|:------------|
| user | The host was specified by the user |
| vc | The host was selected by Virtual Center |
| drs | The host was selected by DRS |


<a name='vim.vm.guest.FileManager.FileInfo.FileType'>GuestFileType</a> - vim.vm.guest.FileManager.FileInfo
==========================================================================================================
| name | description |
|:-----|:------------|
| file | normal file |
| directory | directory |
| symlink | symbolic link |


<a name='vim.vm.GuestInfo.AppStateType'>GuestInfoAppStateType</a> - vim.vm.GuestInfo
====================================================================================
Application state type.
| name | description |
|:-----|:------------|
| none | The application state wasn't set from the guest by the application agent.  This is the default. |
| appStateOk | The guest's application agent declared its state as normal and doesn't  require any action |
| appStateNeedReset | Guest's application agent asks for immediate reset |


<a name='vim.vm.GuestOsDescriptor.FirmwareType'>GuestOsDescriptorFirmwareType</a> - vim.vm.GuestOsDescriptor
============================================================================================================
Firmware types
| name | description |
|:-----|:------------|
| bios | BIOS firmware |
| efi | Extensible Firmware Interface |


<a name='vim.vm.GuestOsDescriptor.SupportLevel'>GuestOsDescriptorSupportLevel</a> - vim.vm.GuestOsDescriptor
============================================================================================================
Guest OS support level
| name | description |
|:-----|:------------|
| experimental | This operating system is not supported,  but may be supported in the future. |
| legacy | This operating system is not fully supported,  but may have been supported in the past. |
| terminated | No longer supported. |
| supported | Fully supported. |
| unsupported | This operating system is not supported. |
| deprecated | Support for this operating system will be terminated in the future.  Please migrate to using a different operating system. |
| techPreview | This operating system may not be supported yet,  please check VMware compatibility guide. |


<a name='vim.host.ActiveDirectoryInfo.DomainMembershipStatus'>HostActiveDirectoryInfoDomainMembershipStatus</a> - vim.host.ActiveDirectoryInfo
==============================================================================================================================================
| name | description |
|:-----|:------------|
| unknown | The Active Directory integration provider does not support  domain trust checks. |
| ok | No problems with the domain membership. |
| noServers | The host thinks it's part of a domain,  but no domain controllers could be reached to confirm. |
| clientTrustBroken | The client side of the trust relationship is broken. |
| serverTrustBroken | The server side of the trust relationship is broken  (or bad machine password). |
| inconsistentTrust | Unexpected domain controller responded. |
| otherProblem | There's some problem with the domain membership. |


<a name='vim.host.Capability.FtUnsupportedReason'>HostCapabilityFtUnsupportedReason</a> - vim.host.Capability
=============================================================================================================
Set of possible values for   <a href="vim.host.Capability.md#ftCompatibilityIssues">ftCompatibilityIssues</a>
| name | description |
|:-----|:------------|
| vMotionNotLicensed | No VMotion license |
| missingVMotionNic | VMotion nic is not configured on the host |
| missingFTLoggingNic | FT logging nic is not configured on the host |
| ftNotLicensed | Host does not have proper FT license |
| haAgentIssue | Host does not have HA agent running properly |


<a name='vim.host.Capability.VmDirectPathGen2UnsupportedReason'>HostCapabilityVmDirectPathGen2UnsupportedReason</a> - vim.host.Capability
=========================================================================================================================================
Set of possible values for <a href="vim.host.Capability.md#vmDirectPathGen2UnsupportedReason">vmDirectPathGen2UnsupportedReason</a>.
| name | description |
|:-----|:------------|
| hostNptIncompatibleProduct | The host software does not support VMDirectPath Gen 2. |
| hostNptIncompatibleHardware | The host hardware does not support VMDirectPath Gen 2. Note that   this is a general capability for the host and is independent of   support by a given physical NIC. |
| hostNptDisabled | The host is configured to disable VMDirectPath Gen 2. |


<a name='vim.host.ConfigChange.Mode'>HostConfigChangeMode</a> - vim.host.ConfigChange
=====================================================================================
This is a global mode on a configuration specification indicating    whether the structure represents the desired state or the set of    operations to apply on the managed object.   <p>
| name | description |
|:-----|:------------|
| modify | Indicates that the structure represents the    set of operations to apply on the managed object. |
| replace | Indicates that the structure represents the    desired state of the managed object. |


<a name='vim.host.ConfigChange.Operation'>HostConfigChangeOperation</a> - vim.host.ConfigChange
===============================================================================================
This list indicates the operation that should be performed for a    network entity.   <p>
| name | description |
|:-----|:------------|
| add | Indicates the addition of a network entity to    the configuration. |
| remove | Indicates the removal of a network entity from    the configuration. |
| edit | Indicates changes on the network entity.  The    entity must exist or a <a href="vim.fault.NotFound.md">NotFound</a> error   will be thrown. |


<a name='vim.host.CpuPackage.Vendor'>HostCpuPackageVendor</a> - vim.host.CpuPackage
===================================================================================
| name | description |
|:-----|:------------|
| unknown | unknown |
| intel | intel |
| amd | amd |


<a name='vim.host.CpuPowerManagementInfo.PolicyType'>HostCpuPowerManagementInfoPolicyType</a> - vim.host.CpuPowerManagementInfo
===============================================================================================================================
Possible values for Current CPU power management policy
| name | description |
|:-----|:------------|
| off | off |
| staticPolicy | staticPolicy |
| dynamicPolicy | dynamicPolicy |


<a name='vim.event.HostDasErrorEvent.HostDasErrorReason'>HostDasErrorEventHostDasErrorReason</a> - vim.event.HostDasErrorEvent
==============================================================================================================================
| name | description |
|:-----|:------------|
| configFailed | Error while configuring/unconfiguring HA |
| timeout | Timeout while communicating with HA agent |
| communicationInitFailed | HA communication initialization failed |
| healthCheckScriptFailed | Health check script failed |
| agentFailed | HA agent has an error |
| agentShutdown | HA agent was shutdown |
| isolationAddressUnpingable | HA isolation address unpingable |
| other | Other reason |


<a name='vim.host.DigestInfo.DigestMethodType'>HostDigestInfoDigestMethodType</a> - vim.host.DigestInfo
=======================================================================================================
The set of digest methods that can be used by TPM to calculate the PCR   values.
| name | description |
|:-----|:------------|
| SHA1 | SHA1 |
| MD5 | MD5 |


<a name='vim.event.HostDisconnectedEvent.ReasonCode'>HostDisconnectedEventReasonCode</a> - vim.event.HostDisconnectedEvent
==========================================================================================================================
| name | description |
|:-----|:------------|
| sslThumbprintVerifyFailed | Failed to verify SSL thumbprint |
| licenseExpired | License expired for the host |
| agentUpgrade | Agent is being upgraded |
| userRequest | User requested disconnect |
| insufficientLicenses | License not available after host upgrade |
| agentOutOfDate | Agent is out of date |
| passwordDecryptFailure | Failed to decrypt password |
| unknown | Unknown reason |
| vcVRAMCapacityExceeded | The vRAM capacity of vCenter will be exceeded |


<a name='vim.host.DiskPartitionInfo.PartitionFormat'>HostDiskPartitionInfoPartitionFormat</a> - vim.host.DiskPartitionInfo
==========================================================================================================================
List of partition format types. This denotes the partition table layout.
| name | description |
|:-----|:------------|
| gpt | gpt |
| mbr | mbr |
| unknown | unknown |


<a name='vim.host.DiskPartitionInfo.Type'>HostDiskPartitionInfoType</a> - vim.host.DiskPartitionInfo
====================================================================================================
List of symbol partition types
| name | description |
|:-----|:------------|
| none | none |
| vmfs | vmfs |
| linuxNative | linuxNative |
| linuxSwap | linuxSwap |
| extended | extended |
| ntfs | ntfs |
| vmkDiagnostic | vmkDiagnostic |
| vffs | vffs |


<a name='vim.host.FeatureVersionInfo.FeatureVersionKey'>HostFeatureVersionKey</a> - vim.host.FeatureVersionInfo
===============================================================================================================
Set of possible values for  <a href="vim.host.FeatureVersionInfo.md#key">key</a>, which  is a unique key that identifies a feature.
| name | description |
|:-----|:------------|
| faultTolerance | VMware Fault Tolerance feature. For pre-4.1 hosts, the  version value reported will be empty in which case   <a href="vim.AboutInfo.md#build">build</a> should be used. For all   other hosts, the version number reported will be a component-specific  version identifier of the form X.Y.Z, where:  X refers to host agent Fault Tolerance version number,  Y refers to VMX Fault Tolerance version number,  Z refers to VMkernal Fault Tolerance version |


<a name='vim.host.Ruleset.Rule.Direction'>HostFirewallRuleDirection</a> - vim.host.Ruleset.Rule
===============================================================================================
Enumeration of port directions.
| name | description |
|:-----|:------------|
| inbound | inbound |
| outbound | outbound |


<a name='vim.host.Ruleset.Rule.PortType'>HostFirewallRulePortType</a> - vim.host.Ruleset.Rule
=============================================================================================
Enumeration of port types.
| name | description |
|:-----|:------------|
| src | src |
| dst | dst |


<a name='vim.host.Ruleset.Rule.Protocol'>HostFirewallRuleProtocol</a> - vim.host.Ruleset.Rule
=============================================================================================
Set of valid port protocols.
| name | description |
|:-----|:------------|
| tcp | tcp |
| udp | udp |


<a name='vim.host.GraphicsInfo.GraphicsType'>HostGraphicsInfoGraphicsType</a> - vim.host.GraphicsInfo
=====================================================================================================
Possible values for graphics type.
| name | description |
|:-----|:------------|
| basic | Basic graphics when no host driver is available. |
| shared | Shared graphics. |
| direct | Direct graphics (ie. pass through). |


<a name='vim.host.HardwareStatusInfo.Status'>HostHardwareElementStatus</a> - vim.host.HardwareStatusInfo
========================================================================================================
The current status of the hardware
| name | description |
|:-----|:------------|
| Unknown | The implementation cannot report on the current status of the   physical element |
| Green | The physical element is functioning as expected |
| Yellow | All functionality is available but some might be degraded. |
| Red | The physical element is failing. It is possible that some or all   functionalities of this physical element is degraded or not working. |


<a name='vim.host.ImageConfigManager.AcceptanceLevel'>HostImageAcceptanceLevel</a> - vim.host.ImageConfigManager
================================================================================================================
Acceptance level definitions
| name | description |
|:-----|:------------|
| vmware_certified | "VMware-certified" |
| vmware_accepted | "VMware-accepted" |
| partner | "Partner-supported" |
| community | "Community-supported" |


<a name='vim.fault.HostIncompatibleForFaultTolerance.Reason'>HostIncompatibleForFaultToleranceReason</a> - vim.fault.HostIncompatibleForFaultTolerance
======================================================================================================================================================
Reasons why fault tolerance is not supported on the host.
| name | description |
|:-----|:------------|
| product | The product does not support fault tolerance. |
| processor | The product supports fault tolerance but the host CPU does not. |


<a name='vim.fault.HostIncompatibleForRecordReplay.Reason'>HostIncompatibleForRecordReplayReason</a> - vim.fault.HostIncompatibleForRecordReplay
================================================================================================================================================
Reasons why record/replay is not supported on a host.
| name | description |
|:-----|:------------|
| product | The product does not support record/replay. |
| processor | The product supports record/replay but the host CPU does not. |


<a name='vim.host.InternetScsiHba.ChapAuthenticationType'>HostInternetScsiHbaChapAuthenticationType</a> - vim.host.InternetScsiHba
==================================================================================================================================
The type of CHAP authentication setting to use.   prohibited  : do not use CHAP.    preferred   : use CHAP if successfully negotiated,                  but allow non-CHAP connections as fallback   discouraged : use non-CHAP, but allow CHAP connectsion as fallback   required    : use CHAP for connection strictly, and fail if CHAP                 negotiation fails.    Defaults to preferred on first configuration if unspecified.
| name | description |
|:-----|:------------|
| chapProhibited | chapProhibited |
| chapDiscouraged | chapDiscouraged |
| chapPreferred | chapPreferred |
| chapRequired | chapRequired |


<a name='vim.host.InternetScsiHba.DigestType'>HostInternetScsiHbaDigestType</a> - vim.host.InternetScsiHba
==========================================================================================================
The type of integrity checks to use. The digest setting for header    and data traffic can be separately configured.   prohibited  : do not use digest.   preferred   : use digest if successfully negotiated, but skip the use                 of digest otherwise.   discouraged : do not use digest if target allows, otherwise use digest.   required    : use digest strictly, and fail if target does not support                 digest.    Defaults to preferred on first configuration if unspecified.
| name | description |
|:-----|:------------|
| digestProhibited | digestProhibited |
| digestDiscouraged | digestDiscouraged |
| digestPreferred | digestPreferred |
| digestRequired | digestRequired |


<a name='vim.host.InternetScsiHba.NetworkBindingSupportType'>HostInternetScsiHbaNetworkBindingSupportType</a> - vim.host.InternetScsiHba
========================================================================================================================================
The binding mode of the adapter.
| name | description |
|:-----|:------------|
| notsupported | notsupported |
| optional | optional |
| required | required |


<a name='vim.host.InternetScsiHba.StaticTarget.TargetDiscoveryMethod'>HostInternetScsiHbaStaticTargetTargetDiscoveryMethod</a> - vim.host.InternetScsiHba.StaticTarget
======================================================================================================================================================================
The method of discovery of an iScsi target.  staticMethod: static discovery  sendTargetsMethod: sendtarget discovery  slpMethod: Service Location Protocol discovery  isnsMethod: Internet Storage Name Service discovery  unknownMethod: discovery method not identified by iscsi stack
| name | description |
|:-----|:------------|
| staticMethod | staticMethod |
| sendTargetMethod | sendTargetMethod |
| slpMethod | slpMethod |
| isnsMethod | isnsMethod |
| unknownMethod | unknownMethod |


<a name='vim.host.IpConfig.IpV6AddressConfigType'>HostIpConfigIpV6AddressConfigType</a> - vim.host.IpConfig
===========================================================================================================
This specifies how the ipv6 address is configured for the interface.  We follow rfc4293 in defining the values for the configType.
| name | description |
|:-----|:------------|
| other | Any other type of address configuration other than the below   mentioned ones will fall under this category. For e.g., automatic   address configuration for the link local address falls under   this type. |
| manual | The address is configured manually. |
| dhcp | The address is configured through dhcp. |
| linklayer | The address is obtained through stateless autoconfiguration. |
| random | The address is chosen by the system at random   e.g., an IPv4 address within 169.254/16, or an RFC   3041 privacy address. |


<a name='vim.host.IpConfig.IpV6AddressStatus'>HostIpConfigIpV6AddressStatus</a> - vim.host.IpConfig
===================================================================================================
| name | description |
|:-----|:------------|
| preferred | Indicates that this is a valid address. |
| deprecated | Indicates that this is a valid but deprecated address   that should no longer be used as a source address. |
| invalid | Indicates that this isn't a valid. |
| inaccessible | Indicates that the address is not accessible because  interface is not operational. |
| unknown | Indicates that the status cannot be determined. |
| tentative | Indicates that the uniqueness of the   address on the link is presently being verified. |
| duplicate | Indicates the address has been determined to be non-unique  on the link, this address will not be reachable. |


<a name='vim.LicenseManager.LicensableResourceInfo.ResourceKey'>HostLicensableResourceKey</a> - vim.LicenseManager.LicensableResourceInfo
=========================================================================================================================================
Identifiers of currently supported resources.
| name | description |
|:-----|:------------|
| numCpuPackages | Number of CPU packages on this host. |
| numCpuCores | Number of licensable CPU cores/compute-units on this host. |
| memorySize | Total size of memory installed on this host, measured in kilobytes. |
| memoryForVms | Total size of memory configured for VMs on this host, measured in kilobytes. |
| numVmsStarted | Number of VMs already running on this host. |
| numVmsStarting | Number of VMs that are currently powering-on, immigrating, etc. |


<a name='vim.host.LowLevelProvisioningManager.ReloadTarget'>HostLowLevelProvisioningManagerReloadTarget</a> - vim.host.LowLevelProvisioningManager
==================================================================================================================================================
The target of the disk reload.
| name | description |
|:-----|:------------|
| currentConfig | Specifies the reload of the current config of the virtual machine. |
| snapshotConfig | Specifies the reload of the snapshot config of the virtual machine.    If the virtual machine has multiple snapshots, all of the snapshot's   config will be reloaded. |


<a name='vim.host.MountInfo.InaccessibleReason'>HostMountInfoInaccessibleReason</a> - vim.host.MountInfo
========================================================================================================
A datastore can become inaccessible due to a number of reasons as    defined in this enum InaccessibleReason.   The reason for a datastore being inaccessibile is reported in   <a href="vim.host.MountInfo.md#inaccessibleReason">inaccessibleReason</a>.    APD ("All Paths Down") is a condition where a SAN or NFS storage has   become inaccessible for unknown reasons. It only indicates loss of   connectivity and does not indicate storage device failure or   LUN removal (Permanent Device Loss or PDL)    A difference between APD and PDL is that APD may recover   in which case all use cases will start to work as before. In case of PDL   the failed datastore/device is unlikely to recover and hence the device   path information and data cache will be emptied. If the PDL condition   recovers, the failed datastores have to be added back to the host. Once   in PDL a datastore cannot be added back until there are no longer any   open files on the datastore.    PDL is not linked to the APD and can happen at any time with or without APD   preceding. If APD and PDL occur at the same time, APD  will be reported first.   Once (and if) the APD condition clears, PermanentDataLoss will be reported if   PDL condition still exists.
| name | description |
|:-----|:------------|
| AllPathsDown_Start | AllPathsDown_Start value is reported when all paths down state is detected |
| AllPathsDown_Timeout | After a wait for a system default time (which is user modifiable)   to ascertain the state is indeed an APD, AllPathsDown_Timeout property   is reported. The host advanced option used to set timeout period   is "/Misc/APDTimeout"    After the datastore property is set to AllPathsDown_Timeout, all data i/o   to the datastore will be fast-failed (failed immediately). |
| PermanentDeviceLoss | A PDL condition is reported as PermanentDeviceLoss. |


<a name='vim.host.MountInfo.AccessMode'>HostMountMode</a> - vim.host.MountInfo
==============================================================================
Defines the access mode of the datastore.
| name | description |
|:-----|:------------|
| readWrite | The host system has read/write access to the file system. |
| readOnly | The host system has read-only access to the file system. |


<a name='vim.host.NetStackInstance.CongestionControlAlgorithmType'>HostNetStackInstanceCongestionControlAlgorithmType</a> - vim.host.NetStackInstance
=====================================================================================================================================================
Define TCP congestion control algorithm used by an instance
| name | description |
|:-----|:------------|
| newreno | New Reno Algorithm.    See http://tools.ietf.org/html/rfc3782 for detail. |
| cubic | Cubic Algorithm.    See http://tools.ietf.org/id/draft-rhee-tcp-cubic-00.txt for detail. |


<a name='vim.host.NetStackInstance.SystemStackKey'>HostNetStackInstanceSystemStackKey</a> - vim.host.NetStackInstance
=====================================================================================================================
Define the instance identifier for different traffic type
| name | description |
|:-----|:------------|
| defaultTcpipStack | The default stack used by applications |


<a name='vim.host.NumericSensorInfo.HealthState'>HostNumericSensorHealthState</a> - vim.host.NumericSensorInfo
==============================================================================================================
Health state of the numeric sensor as reported by the sensor probes.
| name | description |
|:-----|:------------|
| unknown | The implementation cannot report on the current health state of the   physical element |
| green | The sensor is operating under normal conditions |
| yellow | The sensor is operating under conditions that are non-critical. |
| red | The sensor is operating under critical or fatal conditions. This may    directly affect the functioning of both the sensor and related    components. |


<a name='vim.host.NumericSensorInfo.SensorType'>HostNumericSensorType</a> - vim.host.NumericSensorInfo
======================================================================================================
| name | description |
|:-----|:------------|
| fan | Fan sensor |
| power | Power sensor |
| temperature | Temperature sensor |
| voltage | Voltage Sensor |
| other | Other sensor. |


<a name='vim.host.PatchManager.Status.InstallState'>HostPatchManagerInstallState</a> - vim.host.PatchManager.Status
===================================================================================================================
The installation state if the update is installed on the server.
| name | description |
|:-----|:------------|
| hostRestarted | The server has been restarted since the update installation. |
| imageActive | Indicates if the newly installed image is active on the server |


<a name='vim.host.PatchManager.Status.Integrity'>HostPatchManagerIntegrityStatus</a> - vim.host.PatchManager.Status
===================================================================================================================
The integrity validation status.
| name | description |
|:-----|:------------|
| validated | The update is successfully validated. |
| keyNotFound | The integrity can not be verified since a public key to   verify the update cannot be found. |
| keyRevoked | A public key to verify the update has been revoked. |
| keyExpired | A public key to verify the update is expired. |
| digestMismatch | A digital signature of the update does not match. |
| notEnoughSignatures | Not enough signed signatures on the update. |
| validationError | The integrity validation failed. |


<a name='vim.host.PatchManager.Status.Reason'>HostPatchManagerReason</a> - vim.host.PatchManager.Status
=======================================================================================================
Reasons why an update is not applicable to the ESX host.
| name | description |
|:-----|:------------|
| obsoleted | The update is made obsolete by other patches installed on the host. |
| missingPatch | The update depends on another update that is neither installed   nor in the scanned list of updates. |
| missingLib | The update depends on certain libraries or RPMs that are not   available. |
| hasDependentPatch | The update depends on an update that is not installed but is   in the scanned list of updates. |
| conflictPatch | The update conflicts with certain updates that are already   installed on the host. |
| conflictLib | The update conflicts with RPMs or libraries installed on the   host. |


<a name='vim.cluster.HostPowerAction.OperationType'>HostPowerOperationType</a> - vim.cluster.HostPowerAction
============================================================================================================
| name | description |
|:-----|:------------|
| powerOn | Power On Operation |
| powerOff | Power Off Operation. Power off operation puts the host in  a state that can be woken up remotely. |


<a name='vim.profile.host.ProfileManager.AnswerFileStatus'>HostProfileManagerAnswerFileStatus</a> - vim.profile.host.ProfileManager
===================================================================================================================================
The <a href="vim.profile.host.ProfileManager.AnswerFileStatus.md">HostProfileManagerAnswerFileStatus</a> enum  defines possible values for answer file status.
| name | description |
|:-----|:------------|
| valid | Answer file is valid. |
| invalid | Answer file is not valid. The file is either missing or incomplete.  <ul>  <li>To produce an answer file, pass host-specific data (user input) to the  <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a>.<a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a>  method.</li><br/>  <li>To produce a complete answer file, call the  <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a>  method and fill in any missing parameters in the returned  <a href="vim.profile.host.ExecuteResult.md">ProfileExecuteResult</a>.<a href="vim.profile.host.ExecuteResult.md#requireInput">requireInput</a>  list. After you execute the profile successfully, you can pass the complete required  input list to the apply method.</li>  </ul> |
| unknown | Answer file status is not known. |


<a name='vim.host.Capability.ReplayUnsupportedReason'>HostReplayUnsupportedReason</a> - vim.host.Capability
===========================================================================================================
Set of possible values for  <a href="vim.host.Capability.md#replayUnsupportedReason">replayUnsupportedReason</a> and  <a href="vim.host.Capability.md#replayCompatibilityIssues">replayCompatibilityIssues</a>.
| name | description |
|:-----|:------------|
| incompatibleProduct | incompatibleProduct |
| incompatibleCpu | incompatibleCpu |
| hvDisabled | hvDisabled |
| cpuidLimitSet | cpuidLimitSet |
| oldBIOS | oldBIOS |
| unknown | unknown |


<a name='vim.host.RuntimeInfo.NetStackInstanceRuntimeInfo.State'>HostRuntimeInfoNetStackInstanceRuntimeInfoState</a> - vim.host.RuntimeInfo.NetStackInstanceRuntimeInfo
=======================================================================================================================================================================
Define the instance state type
| name | description |
|:-----|:------------|
| inactive | The instance is deleted or not running |
| active | The instance is running |
| deactivating | The instance is in the progress of asynchronous deletion |
| activating | Reserved state for future proofing asynchronous creation |


<a name='vim.host.Service.Policy'>HostServicePolicy</a> - vim.host.Service
==========================================================================
Set of valid service policy strings.
| name | description |
|:-----|:------------|
| on | Service should be started when the host starts up. |
| automatic | Service should run if and only if it has open firewall ports. |
| off | Service should not be started when the host starts up. |


<a name='vim.host.SnmpSystem.AgentLimits.Capability'>HostSnmpAgentCapability</a> - vim.host.SnmpSystem.AgentLimits
==================================================================================================================
SNMP Agent supported capabilities enum
| name | description |
|:-----|:------------|
| COMPLETE | Implements test notifications and allows agent configuration |
| DIAGNOSTICS | Implements only test notification capability only |
| CONFIGURATION | Allows for agent configuration only |


<a name='vim.HostSystem.StandbyMode'>HostStandbyMode</a> - vim.HostSystem
=========================================================================
Defines a host's standby mode.
| name | description |
|:-----|:------------|
| entering | The host is entering standby mode. |
| exiting | The host is exiting standby mode. |
| in | The host is in standby mode. |
| none | The host is not in standy mode. And it is not   in the process of entering/exiting standby mode. |


<a name='vim.HostSystem.ConnectionState'>HostSystemConnectionState</a> - vim.HostSystem
=======================================================================================
Defines a host's connection state.
| name | description |
|:-----|:------------|
| connected | Connected to the server. For ESX Server, this is always the setting. |
| notResponding | VirtualCenter is not receiving heartbeats from the server. The state   automatically changes to connected once heartbeats are received   again. This state is typically used to trigger an alarm on the host. |
| disconnected | The user has explicitly taken the host down. VirtualCenter does not expect to   receive heartbeats from the host. The next time a heartbeat is received, the   host is moved to the connected state again and an event is logged. |


<a name='vim.host.SystemIdentificationInfo.Identifier'>HostSystemIdentificationInfoIdentifier</a> - vim.host.SystemIdentificationInfo
=====================================================================================================================================
| name | description |
|:-----|:------------|
| AssetTag | The Asset tag of the system |
| ServiceTag | The Service tag of the system |
| OemSpecificString | OEM specific string |


<a name='vim.HostSystem.PowerState'>HostSystemPowerState</a> - vim.HostSystem
=============================================================================
Defines a host's power state.
| name | description |
|:-----|:------------|
| poweredOn | The host is powered on. A host that is entering standby mode  <a href="vim.HostSystem.StandbyMode.md#entering">entering</a> is also in this state. |
| poweredOff | The host was specifically powered off by the user through  VirtualCenter. This state is not a cetain state, because  after VirtualCenter issues the command to power off the host,  the host might crash, or kill all the processes but fail to  power off. |
| standBy | The host was specifically put in standby mode, either  explicitly by the user, or automatically by DPM. This state  is not a cetain state, because after VirtualCenter issues the  command to put the host in standby state, the host might  crash, or kill all the processes but fail to power off. A host  that is exiting standby mode <a href="vim.HostSystem.StandbyMode.md#exiting">exiting</a>  is also in this state. |
| unknown | If the host is disconnected, or notResponding, we cannot  possibly have knowledge of its power state. Hence, the host  is marked as unknown. |


<a name='vim.host.UnresolvedVmfsExtent.UnresolvedReason'>HostUnresolvedVmfsExtentUnresolvedReason</a> - vim.host.UnresolvedVmfsExtent
=====================================================================================================================================
Reasons for identifying the disk extent   as copy of VMFS volume extent.
| name | description |
|:-----|:------------|
| diskIdMismatch | The VMFS detected 'diskid' does not match with   LVM detected 'diskId' |
| uuidConflict | VMFS 'uuid' does not match |


<a name='vim.host.UnresolvedVmfsResolutionSpec.VmfsUuidResolution'>HostUnresolvedVmfsResolutionSpecVmfsUuidResolution</a> - vim.host.UnresolvedVmfsResolutionSpec
=================================================================================================================================================================
| name | description |
|:-----|:------------|
| resignature | Resignature the Unresolved VMFS volume.   <p>   In the event the volume to be resignatured contains multiple   extents but only a single copy of each extent exists, only the   head extent needs to be specified. |
| forceMount | Keep the original Uuid of the VMFS volume and mount it   <p>   In the event the volume to be force mounted contains multiple   extents but only a single copy of each extent exists, only the   head extent needs to be specified. |


<a name='vim.host.VirtualNicManager.NicType'>HostVirtualNicManagerNicType</a> - vim.host.VirtualNicManager
==========================================================================================================
| name | description |
|:-----|:------------|
| vmotion | The VirtualNic is used for VMotion. |
| faultToleranceLogging | The VirtualNic is used for Fault Tolerance logging. |
| vSphereReplication | The VirtualNic is used for vSphere Replication LWD traffic  (i.e From the primary host to the VR server). |
| management | The VirtualNic is used for management network traffic .   This nicType is available only when the system does not   support service console adapters.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| vsan | The VirtualNic is used for VSAN traffic.  To enable or disable a VirtualNic for VSAN networking,  use <a href="vim.host.VsanSystem.md#update">UpdateVsan_Task</a>.<br>See <a href="vim.host.VsanSystem.md">HostVsanSystem</a><br>See <a href="vim.host.VsanSystem.md#update">UpdateVsan_Task</a><br>See <a href="vim.ComputeResource.md#reconfigureEx">ReconfigureComputeResource_Task</a><br> |


<a name='vim.host.VmciAccessManager.Mode'>HostVmciAccessManagerMode</a> - vim.host.VmciAccessManager
====================================================================================================
Set of possible values for mode field in AccessSpec.
| name | description |
|:-----|:------------|
| grant | Grant access to specified services in addition to existing services. |
| replace | Replace existing services with specified services. |
| revoke | Revoke the specified services. |


<a name='vim.HttpNfcLease.State'>HttpNfcLeaseState</a> - vim.HttpNfcLease
=========================================================================
List of possible states of a lease.
| name | description |
|:-----|:------------|
| initializing | When the lease is being initialized. |
| ready | When the lease is ready and disks may be transferred. |
| done | When the import/export session is completed, and the lease  is no longer held. |
| error | When an error has occurred. |


<a name='vim.host.InternetScsiHba.DiscoveryProperties.ISnsDiscoveryMethod'>InternetScsiSnsDiscoveryMethod</a> - vim.host.InternetScsiHba.DiscoveryProperties
============================================================================================================================================================
The available iSNS discovery methods.
| name | description |
|:-----|:------------|
| isnsStatic | isnsStatic |
| isnsDhcp | isnsDhcp |
| isnsSlp | isnsSlp |


<a name='vim.fault.InvalidDasConfigArgument.EntryForInvalidArgument'>InvalidDasConfigArgumentEntryForInvalidArgument</a> - vim.fault.InvalidDasConfigArgument
=============================================================================================================================================================
| name | description |
|:-----|:------------|
| admissionControl | Policies for admission control |
| userHeartbeatDs | User-specified heartbeat datastores |
| vmConfig | VM override |


<a name='vim.fault.InvalidProfileReferenceHost.Reason'>InvalidProfileReferenceHostReason</a> - vim.fault.InvalidProfileReferenceHost
====================================================================================================================================
| name | description |
|:-----|:------------|
| incompatibleVersion | The associated host and profile version are incompatible. |
| missingReferenceHost | There is no reference host associated with the profile. |


<a name='vim.host.IscsiManager.IscsiPortInfo.PathStatus'>IscsiPortInfoPathStatus</a> - vim.host.IscsiManager.IscsiPortInfo
==========================================================================================================================
| name | description |
|:-----|:------------|
| notUsed | There are no paths on this Virtual NIC |
| active | All paths on this Virtual NIC are standby paths from SCSI stack  perspective. |
| standBy | One or more paths on the Virtual NIC are active paths to  storage. Unbinding this Virtual NIC will cause storage path  transitions. |
| lastActive | One or more paths on the Virtual NIC is the last active  path to a particular storage device. |


<a name='vim.LatencySensitivity.SensitivityLevel'>LatencySensitivitySensitivityLevel</a> - vim.LatencySensitivity
=================================================================================================================
Enumeration of the nominal latency-sensitive values which can be   used to specify the latency-sensitivity level of the application.   <p />   In terms of latency-sensitivity the values relate:   high>medium>normal>low.
| name | description |
|:-----|:------------|
| low | The relative latency-sensitivity low value. |
| normal | The relative latency-sensitivity normal value.   <p>   This is the default latency-sensitivity value. |
| medium | The relative latency-sensitivity medium value. |
| high | The relative latency-sensitivity high value. |
| custom | deprecated as of vSphere API Ver 5.5.  Value will be ignored and   treated as "normal" latency sensitivity.    The custom absolute latency-sensitivity specified in   <a href="vim.LatencySensitivity.md#sensitivity">sensitivity</a> property is used to   define the latency-sensitivity.   <p />   When this value is set to <a href="vim.LatencySensitivity.md#level">level</a> the   <a href="vim.LatencySensitivity.md#sensitivity">sensitivity</a> property should be   set also. |


<a name='vim.fault.LicenseAssignmentFailed.Reason'>LicenseAssignmentFailedReason</a> - vim.fault.LicenseAssignmentFailed
========================================================================================================================
| name | description |
|:-----|:------------|
| keyEntityMismatch | The license and the entity to which it is to be assigned are not compatible. |
| downgradeDisallowed | The license downgrade is disallowed because some features are in use. |
| inventoryNotManageableByVirtualCenter | The inventory has hosts which are not manageable by vCenter unless in evaluation. |
| hostsUnmanageableByVirtualCenterWithoutLicenseServer | The inventory has hosts that need the license server to be configured unless vCenter is in evaluation |


<a name='vim.LicenseManager.FeatureInfo.SourceRestriction'>LicenseFeatureInfoSourceRestriction</a> - vim.LicenseManager.FeatureInfo
===================================================================================================================================
Some licenses may only be allowed to load from a specified source.   This enum indicates what restrictions exist for this license if any.
| name | description |
|:-----|:------------|
| unrestricted | The feature does not have a source restriction. |
| served | The feature's license can only be served. |
| file | The feature's license can only come from a file. |


<a name='vim.LicenseManager.FeatureInfo.State'>LicenseFeatureInfoState</a> - vim.LicenseManager.FeatureInfo
===========================================================================================================
Describes the state of the feature.
| name | description |
|:-----|:------------|
| enabled | The current edition license has implicitly enabled this additional feature. |
| disabled | The current edition license does not allow this additional feature. |
| optional | The current edition license allows this additional feature. The   <a href="vim.LicenseManager.FeatureInfo.md#enable">EnableFeature</a> and <a href="vim.LicenseManager.FeatureInfo.md#disable">DisableFeature</a> methods can be used to enable or disable   this feature. |


<a name='vim.LicenseManager.FeatureInfo.CostUnit'>LicenseFeatureInfoUnit</a> - vim.LicenseManager.FeatureInfo
=============================================================================================================
Cost units apply to licenses for the purpose of determining   how many licenses are needed.
| name | description |
|:-----|:------------|
| host | One license is acquired per host. |
| cpuCore | One license is acquired per CPU core. |
| cpuPackage | One license is acquired per CPU package. |
| server | One license is acquired per server. |
| vm | One license is acquired per virtual machine. |


<a name='vim.LicenseManager.LicenseKey'>LicenseManagerLicenseKey</a> - vim.LicenseManager
=========================================================================================
Licensed features have unique keys to identify them.
| name | description |
|:-----|:------------|
| esxFull | The edition license for the ESX Server, Standard edition. This is a per    CPU package license. |
| esxVmtn | The edition license for the ESX server, VMTN edition. This is a per CPU package    license. |
| esxExpress | The edition license for the ESX server, Starter edition. This is a per CPU    package license. |
| san | Enable use of SAN. This is a per CPU package license. |
| iscsi | Enable use of iSCSI. This is a per CPU package license. |
| nas | Enable use of NAS. This is a per CPU package license. |
| vsmp | Enable up to 4-way VSMP feature. This is a per CPU package license. |
| backup | Enable ESX Server consolidated backup feature. This is a per CPU package    license. |
| vc | The edition license for a VirtualCenter server, full edition. This license   is independent of the number of CPU packages for the VirtualCenter host. |
| vcExpress | The edition license for a VirtualCenter server, starter edition. This license   limits the number of hosts (esxHost or serverHost) that can be managed by the   VirtualCenter product. |
| esxHost | Enable VirtualCenter ESX Server host management functionality. This is a per    ESX server CPU package license. |
| gsxHost | Enable VirtualCenter GSX Server host management functionality. This is a per    GSX server CPU package license. |
| serverHost | Enable VirtualCenter VMware server host management functionality. This is a per   VMware server CPU package license. |
| drsPower | Enable VirtualCenter DRS Power Management Functionality. This is a per CPU package |
| vmotion | Enable VMotion. This is a per ESX server CPU package license. |
| drs | Enable VirtualCenter Distributed Resource Scheduler. This is a per ESX server    CPU package license. |
| das | Enable VirtualCenter HA. This is a per ESX server CPU package license. |


<a name='vim.LicenseManager.LicenseState'>LicenseManagerState</a> - vim.LicenseManager
======================================================================================
State of licensing subsystem.
| name | description |
|:-----|:------------|
| initializing | Setting or resetting configuration in progress. |
| normal | Running within operating parameters. |
| marginal | License source unavailable, using license cache. |
| fault | Initialization has failed or grace period expired. |


<a name='vim.LicenseManager.ReservationInfo.State'>LicenseReservationInfoState</a> - vim.LicenseManager.ReservationInfo
=======================================================================================================================
Describes the reservation state of a license.
| name | description |
|:-----|:------------|
| notUsed | This license is currently unused by the system, or the feature does not   apply. For example, a DRS license appears as NotUsed if the host is not   part of a DRS-enabled cluster. |
| noLicense | This indicates that the license has expired or the system attempted to acquire   the license but was not successful in reserving it. |
| unlicensedUse | The LicenseManager failed to acquire a license but the implementation   policy allows us to use the licensed feature anyway. This is possible, for   example, when a license server becomes unavailable after a license had been   successfully reserved from it. |
| licensed | The required number of licenses have been acquired from the license source. |


<a name='vim.host.LinkDiscoveryProtocolConfig.OperationType'>LinkDiscoveryProtocolConfigOperationType</a> - vim.host.LinkDiscoveryProtocolConfig
================================================================================================================================================
The Discovery Protocol operation.
| name | description |
|:-----|:------------|
| none | Don't listen for incoming discovery packets and don't sent  discover   packets for the switch either. |
| listen | Listen for incoming discovery packets but don't sent discovery packet   for the switch. |
| advertise | Sent discovery packets for the switch, but don't listen for incoming   discovery packets. |
| both | Sent discovery packets for the switch and listen for incoming   discovery packets. |


<a name='vim.host.LinkDiscoveryProtocolConfig.ProtocolType'>LinkDiscoveryProtocolConfigProtocolType</a> - vim.host.LinkDiscoveryProtocolConfig
==============================================================================================================================================
The Discovery Protocol types.
| name | description |
|:-----|:------------|
| cdp | Cisco Discovery Protocol |
| lldp | Link Layer Discovery Protocol |


<a name='vim.ManagedEntity.Status'>ManagedEntityStatus</a> - vim.ManagedEntity
==============================================================================
The Status enumeration defines a general "health" value for a managed entity.
| name | description |
|:-----|:------------|
| gray | The status is unknown. |
| green | The entity is OK. |
| yellow | The entity might have a problem. |
| red | The entity definitely has a problem. |


<a name='vim.alarm.MetricAlarmExpression.MetricOperator'>MetricAlarmOperator</a> - vim.alarm.MetricAlarmExpression
==================================================================================================================
The operation on the target metric item.
| name | description |
|:-----|:------------|
| isAbove | Test if the target metric item is above the given red or yellow values. |
| isBelow | Test if the target metric item is below the given red or yellow values. |


<a name='vim.host.MultipathInfo.PathState'>MultipathState</a> - vim.host.MultipathInfo
======================================================================================
Set of constants defining the possible states of a multipath path.
| name | description |
|:-----|:------------|
| standby | standby |
| active | active |
| disabled | disabled |
| dead | dead |
| unknown | unknown |


<a name='vim.net.NetBIOSConfigInfo.Mode'>NetBIOSConfigInfoMode</a> - vim.net.NetBIOSConfigInfo
==============================================================================================
NetBIOS configuration mode.
| name | description |
|:-----|:------------|
| unknown | Mode of NetBIOS is unknown. |
| enabled | NetBIOS is enabled. |
| disabled | NetBIOS is disabled. |
| enabledViaDHCP | DHCP server decides whether or not to use NetBIOS. |


<a name='vim.net.IpConfigInfo.IpAddressOrigin'>NetIpConfigInfoIpAddressOrigin</a> - vim.net.IpConfigInfo
========================================================================================================
This specifies how an IP address was obtained for a given interface.  See RFC 4293 IpAddressOriginTC.
| name | description |
|:-----|:------------|
| other | Any other type of address configuration other than the below   mentioned ones will fall under this category. For e.g., automatic   address configuration for the link local address falls under   this type. |
| manual | The address is configured manually. The term 'static' is a synonym. |
| dhcp | The address is configured through dhcp. |
| linklayer | The address is obtained through stateless autoconfiguration (autoconf).  See RFC 4862, IPv6 Stateless Address Autoconfiguration. |
| random | The address is chosen by the system at random   e.g., an IPv4 address within 169.254/16, or an RFC 3041 privacy address. |


<a name='vim.net.IpConfigInfo.IpAddressStatus'>NetIpConfigInfoIpAddressStatus</a> - vim.net.IpConfigInfo
========================================================================================================
| name | description |
|:-----|:------------|
| preferred | Indicates that this is a valid address. |
| deprecated | Indicates that this is a valid but deprecated address   that should no longer be used as a source address. |
| invalid | Indicates that this isn't a valid. |
| inaccessible | Indicates that the address is not accessible because  interface is not operational. |
| unknown | Indicates that the status cannot be determined. |
| tentative | Indicates that the uniqueness of the   address on the link is presently being verified. |
| duplicate | Indicates the address has been determined to be non-unique  on the link, this address will not be reachable. |


<a name='vim.net.IpStackInfo.EntryType'>NetIpStackInfoEntryType</a> - vim.net.IpStackInfo
=========================================================================================
IP Stack keeps state on entries in IpNetToMedia table to perform  physical address lookups for IP addresses. Here are the standard  states per<br>See RFC
| name | description |
|:-----|:------------|
| other | This implementation is reporting something other than  what states are listed below. |
| invalid | The IP Stack has marked this entry as not useable. |
| dynamic | This entry has been learned using ARP or NDP. |
| manual | This entry was set manually. |


<a name='vim.net.IpStackInfo.Preference'>NetIpStackInfoPreference</a> - vim.net.IpStackInfo
===========================================================================================
The set of values used to determine ordering of default routers.   See RFC 4293 ipDefaultRouterPreference.
| name | description |
|:-----|:------------|
| reserved | reserved |
| low | low |
| medium | medium |
| high | high |


<a name='vim.fault.NotSupportedDeviceForFT.DeviceType'>NotSupportedDeviceForFTDeviceType</a> - vim.fault.NotSupportedDeviceForFT
================================================================================================================================
| name | description |
|:-----|:------------|
| virtualVmxnet3 | vmxnet3 virtual Ethernet adapter |
| paraVirtualSCSIController | paravirtualized SCSI controller |


<a name='vim.fault.NumVirtualCpusIncompatible.Reason'>NumVirtualCpusIncompatibleReason</a> - vim.fault.NumVirtualCpusIncompatible
=================================================================================================================================
Reasons why the number of virtual CPUs is incompatible.
| name | description |
|:-----|:------------|
| recordReplay | recordReplay |
| faultTolerance | faultTolerance |


<a name='vmodl.query.PropertyCollector.ObjectUpdate.Kind'>ObjectUpdateKind</a> - vmodl.query.PropertyCollector.ObjectUpdate
===========================================================================================================================
Enumeration of different kinds of updates.
| name | description |
|:-----|:------------|
| modify | A property of the managed object changed its value. |
| enter | A managed object became visible to a filter for the first time.   For instance, this can happen if a virtual machine is added to a   folder. |
| leave | A managed object left the set of objects visible to a filter.  For   instance, this can happen when a virtual machine is destroyed. |


<a name='vim.OvfConsumer.OstNodeType'>OvfConsumerOstNodeType</a> - vim.OvfConsumer
==================================================================================
The type of an OST node.  <p>  Each OST node corresponds to an element in the OVF descriptor. See OstNode  for a description of the different node types.
| name | description |
|:-----|:------------|
| envelope | envelope |
| virtualSystem | virtualSystem |
| virtualSystemCollection | virtualSystemCollection |


<a name='vim.OvfManager.CreateImportSpecParams.DiskProvisioningType'>OvfCreateImportSpecParamsDiskProvisioningType</a> - vim.OvfManager.CreateImportSpecParams
==============================================================================================================================================================
Types of disk provisioning that can be set for the disk in the deployed OVF  package.
| name | description |
|:-----|:------------|
| monolithicSparse | A sparse (allocate on demand) monolithic disk. Disks in this format can  be used with other VMware products. |
| monolithicFlat | A preallocated monolithic disk. Disks in this format can be used with  other VMware products. |
| twoGbMaxExtentSparse | A sparse (allocate on demand) disk with 2GB maximum extent size.  Disks in this format can be used with other VMware products. The 2GB  extent size makes these disks easier to burn to dvd or use on  filesystems that don't support large files. |
| twoGbMaxExtentFlat | A preallocated disk with 2GB maximum extent size. Disks in this format  can be used with other VMware products. The 2GB extent size  makes these disks easier to burn to dvd or use on filesystems that  don't support large files. |
| thin | Space required for thin-provisioned virtual disk is allocated and  zeroed on demand as the space is used. |
| thick | A thick disk has all space allocated at creation time  and the space is zeroed on demand as the space is used. |
| seSparse | A sparse (allocate on demand) format with additional space  optimizations. |
| eagerZeroedThick | An eager zeroed thick disk has all space allocated and wiped clean  of any previous contents on the physical media at creation time.  Such disks may take longer time during creation compared to other  disk formats. |
| sparse | Depending on the host type, Sparse is mapped to either  MonolithicSparse or Thin. |
| flat | Depending on the host type, Flat is mapped to either  MonolithicFlat or Thick. |


<a name='vim.PerformanceManager.Format'>PerfFormat</a> - vim.PerformanceManager
===============================================================================
The format in which performance counter data is returned.
| name | description |
|:-----|:------------|
| normal | Counters returned in an array of data objects. |
| csv | Counters returned in comma-separate value (CSV) format. |


<a name='vim.PerformanceManager.CounterInfo.StatsType'>PerfStatsType</a> - vim.PerformanceManager.CounterInfo
=============================================================================================================
Indicates the type of statistical measurement that a counter&#146;s   value represents. Valid types are &#147;absolute&#148;,   &#147;delta&#148;, or &#147;rate&#148;.
| name | description |
|:-----|:------------|
| absolute | Represents an actual value, level, or state of the counter. For   example, the &#147;uptime&#148; counter (<b>system</b> group)   represents the actual number of seconds since startup. The   &#147;capacity&#148; counter represents the actual configured size   of the specified datastore. In other words, number of samples,   samplingPeriod, and intervals have no bearing on an   &#147;absolute&#148; counter&#147;s value. |
| delta | Represents an amount of change for the counter during the <a href="vim.HistoricalInterval.md#samplingPeriod">samplingPeriod</a> as compared to the previous   <a href="vim.HistoricalInterval.md">interval</a>. The first sampling interval |
| rate | Represents a value that has been normalized over the <a href="vim.HistoricalInterval.md#samplingPeriod">samplingPeriod</a>, enabling values for the same   counter type to be compared, regardless of interval. For example,   the number of reads per second. |


<a name='vim.PerformanceManager.CounterInfo.RollupType'>PerfSummaryType</a> - vim.PerformanceManager.CounterInfo
================================================================================================================
Indicates how multiple samples of a specific counter type are   transformed into a single statistical value.
| name | description |
|:-----|:------------|
| average | The actual value collected or the average of all values collected   during the summary period. |
| maximum | The maximum value of the performance counter value over the   summarization period. |
| minimum | The minimum value of the performance counter value over the   summarization period. |
| latest | The most recent value of the performance counter over the   summarization period. |
| summation | The sum of all the values of the performance counter over the   summarization period. |
| none | The counter is never rolled up. |


<a name='vim.PerformanceManager.CounterInfo.Unit'>PerformanceManagerUnit</a> - vim.PerformanceManager.CounterInfo
=================================================================================================================
Indicates the unit of measure represented by a counter or statistical   value.
| name | description |
|:-----|:------------|
| percent | Percentage values in units of 1/100th of a percent. For example 100   represents 1%. |
| kiloBytes | Kilobytes. |
| megaBytes | Megabytes. |
| megaHertz | Megahertz. |
| number | A quantity of items, for example, the number of CPUs. |
| microsecond | The time in microseconds. |
| millisecond | The time in milliseconds. |
| second | The time in seconds. |
| kiloBytesPerSecond | Kilobytes per second. |
| megaBytesPerSecond | Megabytes per second. |
| watt | Watts |
| joule | Joules |


<a name='vim.host.PhysicalNic.ResourcePoolSchedulerDisallowedReason'>PhysicalNicResourcePoolSchedulerDisallowedReason</a> - vim.host.PhysicalNic
================================================================================================================================================
| name | description |
|:-----|:------------|
| userOptOut | Indicates that the user has opted out the Physical NIC from resource pool   based scheduling. |
| hardwareUnsupported | Indicates that the NIC device does is not capable of resource pool   based scheduling. |


<a name='vim.host.PhysicalNic.VmDirectPathGen2SupportedMode'>PhysicalNicVmDirectPathGen2SupportedMode</a> - vim.host.PhysicalNic
================================================================================================================================
Set of possible values for <a href="vim.host.PhysicalNic.md#vmDirectPathGen2SupportedMode">vmDirectPathGen2SupportedMode</a>.
| name | description |
|:-----|:------------|
| upt | upt |


<a name='vim.host.PortGroup.PortConnecteeType'>PortGroupConnecteeType</a> - vim.host.PortGroup
==============================================================================================
The type of component connected to a port group.
| name | description |
|:-----|:------------|
| virtualMachine | A virtual machine is connected to this port group. |
| systemManagement | A system management entity (service console)   is connected to this port group. |
| host | The VMkernel is connected to this port group. |
| unknown | This port group serves an entity of unspecified kind. |


<a name='vim.profile.host.ExecuteResult.Status'>ProfileExecuteResultStatus</a> - vim.profile.host.ExecuteResult
===============================================================================================================
Defines the result status values for a  <a href="vim.profile.host.HostProfile.md">HostProfile</a>.<a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a>  operation. The result data is contained in the  <a href="vim.profile.host.ExecuteResult.md">ProfileExecuteResult</a> data object.
| name | description |
|:-----|:------------|
| success | Profile execution was successful. You can use the output configuration data  to apply the profile to a host. |
| needInput | Additional data is required to complete the operation.  The data requirements are defined in the list of policy options for the profile  (<a href="vim.profile.ApplyProfile.md">ApplyProfile</a>.<a href="vim.profile.ApplyProfile.md#policy">policy</a>[]). |
| error | Profile execution generated an error.  See <a href="vim.profile.host.ExecuteResult.md">ProfileExecuteResult</a>.<a href="vim.profile.host.ExecuteResult.md#error">error</a>. |


<a name='vim.profile.NumericComparator'>ProfileNumericComparator</a> - None
===========================================================================
Enumerates different operations supported for comparing      numerical values.
| name | description |
|:-----|:------------|
| lessThan | lessThan |
| lessThanEqual | lessThanEqual |
| equal | equal |
| notEqual | notEqual |
| greaterThanEqual | greaterThanEqual |
| greaterThan | greaterThan |


<a name='vmodl.query.PropertyCollector.Change.Op'>PropertyChangeOp</a> - vmodl.query.PropertyCollector.Change
=============================================================================================================
Enumeration of possible changes to a property.
| name | description |
|:-----|:------------|
| add | add |
| remove | remove |
| assign | assign |
| indirectRemove | indirectRemove |


<a name='vim.cluster.Recommendation.ReasonCode'>RecommendationReasonCode</a> - vim.cluster.Recommendation
=========================================================================================================
List of defined migration reason codes:
| name | description |
|:-----|:------------|
| fairnessCpuAvg | Balance average CPU utilization. |
| fairnessMemAvg | Balance average memory utilization. |
| jointAffin | Fulfill affinity rule. |
| antiAffin | Fulfill anti-affinity rule. |
| hostMaint | Host entering maintenance mode. |
| enterStandby | Host entering standby mode. |
| reservationCpu | balance CPU reservations |
| reservationMem | balance memory reservations |
| powerOnVm | Power on virtual machine |
| powerSaving | Power off host for power savings |
| increaseCapacity | Power on host to increase cluster capacity |
| checkResource | Sanity-check resource pool hierarchy |
| unreservedCapacity | Maintain unreserved capacity |
| vmHostHardAffinity | Fix hard VM/host affinity rule violation |
| vmHostSoftAffinity | Fix soft VM/host affinity rule violation |
| balanceDatastoreSpaceUsage | Balance datastore space usage. |
| balanceDatastoreIOLoad | Balance datastore I/O workload. |
| datastoreMaint | Datastore entering maintenance mode. |
| virtualDiskJointAffin | Fix virtual disk affinity rule violation. |
| virtualDiskAntiAffin | Fix virtual disk anti-affinity rule violation. |
| datastoreSpaceOutage | Fix the issue that a datastore run out of space. |
| storagePlacement | Satisfy storage initial placement requests. |
| iolbDisabledInternal | IO load balancing was disabled internally. |


<a name='vim.cluster.Recommendation.RecommendationType'>RecommendationType</a> - vim.cluster.Recommendation
===========================================================================================================
Pre-defined constants for possible recommendation types. Virtual Center   uses this information to coordinate with the clients.
| name | description |
|:-----|:------------|
| V1 | V1 |


<a name='vim.fault.ReplicationDiskConfigFault.ReasonForFault'>ReplicationDiskConfigFaultReasonForFault</a> - vim.fault.ReplicationDiskConfigFault
=================================================================================================================================================
| name | description |
|:-----|:------------|
| diskNotFound | Could not look up device by key |
| diskTypeNotSupported | Replication not supported for disk type or backend |
| invalidDiskKey | Invalid key value |
| invalidDiskReplicationId | Invalid disk replication ID string |
| duplicateDiskReplicationId | Another disk in the VM has the same replication ID |
| invalidPersistentFilePath | Invalid path (string) for the persistent file |
| reconfigureDiskReplicationIdNotAllowed | Attempting to re-configure the disk's replication ID |


<a name='vim.fault.ReplicationVmConfigFault.ReasonForFault'>ReplicationVmConfigFaultReasonForFault</a> - vim.fault.ReplicationVmConfigFault
===========================================================================================================================================
| name | description |
|:-----|:------------|
| incompatibleHwVersion | Incompatible VM hardware version |
| invalidVmReplicationId | Invalid VM Replication ID string |
| invalidGenerationNumber | Invalid generation number in VM's configuration |
| outOfBoundsRpoValue | Invalid RPO value (out of bounds) |
| invalidDestinationIpAddress | Invalid destination IP address |
| invalidDestinationPort | Invalid destination port |
| invalidExtraVmOptions | Malformed extra options list |
| staleGenerationNumber | Mis-matching generation number (stale) |
| reconfigureVmReplicationIdNotAllowed | Attempting to re-configure the VM replication ID |
| cannotRetrieveVmReplicationConfiguration | Could not retrieve the VM configuration |
| replicationAlreadyEnabled | Attempting to re-enable replication for the VM |
| invalidPriorConfiguration | The existing replication configuration of the VM is broken   (applicable to re-configuration only). |
| replicationNotEnabled | Attempting to re-configure or disable replication for a VM  for which replication has not been enabled. |
| replicationConfigurationFailed | Failed to commit the new replication properties for the VM. |


<a name='vim.fault.ReplicationVmFault.ReasonForFault'>ReplicationVmFaultReasonForFault</a> - vim.fault.ReplicationVmFault
=========================================================================================================================
| name | description |
|:-----|:------------|
| notConfigured | <a href="vim.VirtualMachine.md">VirtualMachine</a> is not configured for replication |
| poweredOff | <a href="vim.VirtualMachine.md">VirtualMachine</a> is powered off (and is not undergoing  offline replication) |
| suspended | <a href="vim.VirtualMachine.md">VirtualMachine</a> is suspended (and is not undergoing  offline replication) |
| poweredOn | <a href="vim.VirtualMachine.md">VirtualMachine</a> is powered on |
| offlineReplicating | <a href="vim.VirtualMachine.md">VirtualMachine</a> is in the process of creating an  an offline instance. |
| invalidState | <a href="vim.VirtualMachine.md">VirtualMachine</a> is in an invalid state |
| invalidInstanceId | The specified instanceId does not match the <a href="vim.VirtualMachine.md">VirtualMachine</a>  instanceId |


<a name='vim.HbrManager.ReplicationVmInfo.State'>ReplicationVmState</a> - vim.HbrManager.ReplicationVmInfo
==========================================================================================================
Describes the current state of a replicated <a href="vim.VirtualMachine.md">VirtualMachine</a>
| name | description |
|:-----|:------------|
| none | The <a href="vim.VirtualMachine.md">VirtualMachine</a> has no current replication state.  This is a virtual machine that is configured for replication, but is  powered off and not undergoing offline replication. |
| paused | The <a href="vim.VirtualMachine.md">VirtualMachine</a> replication is paused. |
| syncing | One or more of the <a href="vim.VirtualMachine.md">VirtualMachine</a> disks is in the  process of an initial synchronization with the remote site. |
| idle | The <a href="vim.VirtualMachine.md">VirtualMachine</a> is being replicated but is not  currently in the process of having a consistent instance created. |
| active | The <a href="vim.VirtualMachine.md">VirtualMachine</a> is in the process of having  a consistent instance created. |
| error | The <a href="vim.VirtualMachine.md">VirtualMachine</a> is unable to replicate due to  errors.  <p>  XXX Currently unused. |


<a name='vim.vm.ScheduledHardwareUpgradeInfo.HardwareUpgradePolicy'>ScheduledHardwareUpgradeInfoHardwareUpgradePolicy</a> - vim.vm.ScheduledHardwareUpgradeInfo
===============================================================================================================================================================
The policy setting used to determine when to perform scheduled   upgrades for a virtual machine.
| name | description |
|:-----|:------------|
| never | No scheduled upgrades. |
| onSoftPowerOff | Run scheduled upgrades only on normal guest OS shutdown. |
| always | Always run scheduled upgrades. |


<a name='vim.vm.ScheduledHardwareUpgradeInfo.HardwareUpgradeStatus'>ScheduledHardwareUpgradeInfoHardwareUpgradeStatus</a> - vim.vm.ScheduledHardwareUpgradeInfo
===============================================================================================================================================================
Status for last attempt to run scheduled hardware upgrade.
| name | description |
|:-----|:------------|
| none | No scheduled upgrade ever happened. |
| pending | Upgrade is scheduled, but was not run yet. |
| success | Upgrade succeeded. |
| failed | Upgrade failed.    For more information about the failure<br>See <a href="vim.vm.ScheduledHardwareUpgradeInfo.md#fault">fault</a><br> |


<a name='vim.host.ScsiLun.DescriptorQuality'>ScsiLunDescriptorQuality</a> - vim.host.ScsiLun
============================================================================================
An indicator of the utility of Descriptor in being used as an   identifier that is stable, unique, and correlatable.
| name | description |
|:-----|:------------|
| highQuality | The Descriptor has an identifier that is useful for identification   and correlation across hosts. |
| mediumQuality | The Descriptor has an identifier that may be used for identification   and correlation across hosts. |
| lowQuality | The Descriptor has an identifier that should not be used for   identification and correlation across hosts. |
| unknownQuality | The Descriptor has an identifier that may or may not be useful for   identification and correlation across hosts. |


<a name='vim.host.ScsiLun.State'>ScsiLunState</a> - vim.host.ScsiLun
====================================================================
The Operational state of the LUN
| name | description |
|:-----|:------------|
| unknownState | The LUN state is unknown. |
| ok | The LUN is on and available. |
| error | The LUN is dead and/or not reachable. |
| off | The LUN is off. |
| quiesced | The LUN is inactive. |
| degraded | One or more paths to the LUN are down, but I/O   is still possible.  Further path failures may   result in lost connectivity. |
| lostCommunication | No more paths are available to the LUN. |
| timeout | All Paths have been down for the timeout condition  determined by a user-configurable host advanced option. |


<a name='vim.host.ScsiLun.ScsiLunType'>ScsiLunType</a> - vim.host.ScsiLun
=========================================================================
The list of SCSI device types.  These values correspond to values    published in the SCSI specification.
| name | description |
|:-----|:------------|
| disk | disk |
| tape | tape |
| printer | printer |
| processor | processor |
| worm | worm |
| cdrom | cdrom |
| scanner | scanner |
| opticalDevice | opticalDevice |
| mediaChanger | mediaChanger |
| communications | communications |
| storageArrayController | storageArrayController |
| enclosure | enclosure |
| unknown | unknown |


<a name='vim.host.ScsiLun.VStorageSupportStatus'>ScsiLunVStorageSupportStatus</a> - vim.host.ScsiLun
====================================================================================================
Storage array hardware acceleration support status.   When a host boots, the support status is unknown.   As a host attempts hardware-accelerated operations,   it determines whether the storage device supports hardware acceleration   and sets the <a href="vim.host.ScsiLun.md#vStorageSupport">vStorageSupport</a> property accordingly.
| name | description |
|:-----|:------------|
| vStorageSupported | Storage device supports hardware acceleration.  The ESX host will use the feature to offload certain  storage-related operations to the device. |
| vStorageUnsupported | Storage device does not support hardware acceleration.  The ESX host will handle all storage-related operations. |
| vStorageUnknown | Initial support status value. |


<a name='vim.SessionManager.HttpServiceRequestSpec.Method'>SessionManagerHttpServiceRequestSpecMethod</a> - vim.SessionManager.HttpServiceRequestSpec
=====================================================================================================================================================
HTTP request methods.
| name | description |
|:-----|:------------|
| httpOptions | httpOptions |
| httpGet | httpGet |
| httpHead | httpHead |
| httpPost | httpPost |
| httpPut | httpPut |
| httpDelete | httpDelete |
| httpTrace | httpTrace |
| httpConnect | httpConnect |


<a name='vim.SharesInfo.Level'>SharesLevel</a> - vim.SharesInfo
===============================================================
Simplified shares notation.   These designations have different meanings for different resources.
| name | description |
|:-----|:------------|
| low | For CPU:     Shares = 500 * number of virtual CPUs<br>   For Memory:  Shares =   5 * virtual machine memory size in megabytes<br>   For Disk:    Shares = 500<br>   For Network: Shares = 0.25 * <a href="vim.DistributedVirtualSwitch.FeatureCapability.md#networkResourcePoolHighShareValue">networkResourcePoolHighShareValue</a> |
| normal | For CPU:     Shares = 1000 * number of virtual CPUs<br>   For Memory:  Shares =   10 * virtual machine memory size in megabytes<br>   For Disk:    Shares = 1000<br>   For Network: Shares = 0.5 * <a href="vim.DistributedVirtualSwitch.FeatureCapability.md#networkResourcePoolHighShareValue">networkResourcePoolHighShareValue</a> |
| high | For CPU:     Shares = 2000 * nmumber of virtual CPUs<br>   For Memory:  Shares =   20 * virtual machine memory size in megabytes<br>   For Disk:    Shares = 2000<br>   For Network: Shares = <a href="vim.DistributedVirtualSwitch.FeatureCapability.md#networkResourcePoolHighShareValue">networkResourcePoolHighShareValue</a> |
| custom | If you specify <code>custom</code> for the <a href="vim.SharesInfo.md#level">level</a> property, when there is resource contention the Server uses the <a href="vim.SharesInfo.md#shares">shares</a> value to determine resource allocation. |


<a name='vim.SimpleCommand.Encoding'>SimpleCommandEncoding</a> - vim.SimpleCommand
==================================================================================
The encoding of the resultant return data. This is a hint to the client side   to indicate the format of the information being returned.
| name | description |
|:-----|:------------|
| CSV | Comma separated values |
| HEX | Hex encoded binary data |
| STRING | STRING |


<a name='vim.host.InternetScsiHba.DiscoveryProperties.SlpDiscoveryMethod'>SlpDiscoveryMethod</a> - vim.host.InternetScsiHba.DiscoveryProperties
===============================================================================================================================================
The available SLP discovery methods.
| name | description |
|:-----|:------------|
| slpDhcp | Use DHCP to find the SLP DAs. |
| slpAutoUnicast | Use broadcasting to find SLP DAs.   Only DAs on the current subnet will be found. |
| slpAutoMulticast | Use the well known multicast address to find DAs. |
| slpManual | User specified address for a DA. |


<a name='vim.alarm.StateAlarmExpression.StateOperator'>StateAlarmOperator</a> - vim.alarm.StateAlarmExpression
==============================================================================================================
The operation on the target state.
| name | description |
|:-----|:------------|
| isEqual | Test if the target state matches the given red or yellow states. |
| isUnequal | Test if the target state does not match the given red or yellow states. |


<a name='vim.storageDrs.PodConfigInfo.Behavior'>StorageDrsPodConfigInfoBehavior</a> - vim.storageDrs.PodConfigInfo
==================================================================================================================
Storage DRS behavior.
| name | description |
|:-----|:------------|
| manual | Specifies that VirtualCenter should generate recommendations for   virtual disk migration and for placement with a datastore,   but should not execute the recommendations automatically. |
| automated | Specifies that VirtualCenter should generate recommendations for   virtual disk migration and for placement with a datastore.   The recommendations for virtual disk migrations will be executed automatically,   but the placement recommendations will be done manually. |


<a name='vim.StorageResourceManager.CongestionThresholdMode'>StorageIORMThresholdMode</a> - vim.StorageResourceManager
======================================================================================================================
User specification of congestion threshold mode on a given datastore  <p>  For more information, see  <a href="vim.StorageResourceManager.IORMConfigInfo.md#congestionThreshold">congestionThreshold</a>
| name | description |
|:-----|:------------|
| automatic | Storagage IO Control will choose appropriate congestion threshold value  for that datastore to operate at given percentage of peak throughput.  This is the default setting |
| manual | Use user specified Storage IO Control congestion threshold value |


<a name='vim.storageDrs.StoragePlacementSpec.PlacementType'>StoragePlacementSpecPlacementType</a> - vim.storageDrs.StoragePlacementSpec
=======================================================================================================================================
Defines the storage placement operation type.  <p>
| name | description |
|:-----|:------------|
| create | Create a VM. |
| reconfigure | Reconfigure a VM. |
| relocate | Relocate a VM. |
| clone | Clone a VM. |


<a name='vim.TaskFilterSpec.RecursionOption'>TaskFilterSpecRecursionOption</a> - vim.TaskFilterSpec
===================================================================================================
This option specifies how to select tasks based on child relationships   in the inventory hierarchy. If a managed entity has children, their tasks   can be retrieved with this filter option.
| name | description |
|:-----|:------------|
| self | Returns tasks that pertain only to the specified managed entity,   and not its children. |
| children | Returns tasks pertaining to child entities only. Excludes   tasks pertaining to the specified managed entity itself. |
| all | Returns tasks pertaining either to the specified managed entity   or to its child entities. |


<a name='vim.TaskFilterSpec.TimeOption'>TaskFilterSpecTimeOption</a> - vim.TaskFilterSpec
=========================================================================================
This option specifies a time stamp governing the selection of tasks.
| name | description |
|:-----|:------------|
| queuedTime | The time stamp when the task was created and queued. |
| startedTime | The time stamp when the task started. |
| completedTime | The time stamp when the task finished. |


<a name='vim.TaskInfo.State'>TaskInfoState</a> - vim.TaskInfo
=============================================================
List of possible states of a task.
| name | description |
|:-----|:------------|
| queued | When there are too many tasks for threads to handle. |
| running | When the busy thread is freed from its current task by    finishing the task, it picks a queued task to run.    Then the queued tasks are marked as running. |
| success | When a running task has completed. |
| error | When a running task has encountered an error. |


<a name='vim.fault.ThirdPartyLicenseAssignmentFailed.Reason'>ThirdPartyLicenseAssignmentFailedReason</a> - vim.fault.ThirdPartyLicenseAssignmentFailed
======================================================================================================================================================
| name | description |
|:-----|:------------|
| licenseAssignmentFailed | A general failure has occured during assigning license to the 3rd party module |
| moduleNotInstalled | The 3rd party module we are trying to license is not installed. |


<a name='vim.vm.ToolsConfigInfo.UpgradePolicy'>UpgradePolicy</a> - vim.vm.ToolsConfigInfo
=========================================================================================
The policy setting used to determine when tools are auto-upgraded for   a virtual machine
| name | description |
|:-----|:------------|
| manual | No auto-upgrades for tools will be performed for this    virtual machine. Users must manually invoke the UpgradeTools    operation to update the tools. |
| upgradeAtPowerCycle | When the virtual machine is power-cycled, the system checks    for a newer version of tools when the VM comes back up. If it    is available, a tools upgrade is automatically performed on the    virtual machine and it is rebooted if necessary. |


<a name='vim.vApp.EntityConfigInfo.Action'>VAppAutoStartAction</a> - vim.vApp.EntityConfigInfo
==============================================================================================
| name | description |
|:-----|:------------|
| none | No action is taken for this virtual machine. This virtual machine is   not a part of the auto-start sequence. This can be used for both auto-start   and auto-start settings. |
| powerOn | This virtual machine is powered on when it is next in the auto-start order. |
| powerOff | This virtual machine is powered off when it is next in the auto-stop order.   This is the default stopAction. |
| guestShutdown | The guest operating system for a virtual machine is shut down when that   virtual machine in next in the auto-stop order. |
| suspend | This virtual machine is suspended when it is next in the auto-stop order. |


<a name='vim.vApp.CloneSpec.ProvisioningType'>VAppCloneSpecProvisioningType</a> - vim.vApp.CloneSpec
====================================================================================================
The cloned VMs can either be provisioned the same way as the VMs  they are a clone of, thin provisioned or thick provisioned, or  linked clones (i.e., using delta disks).
| name | description |
|:-----|:------------|
| sameAsSource | Each disk in the cloned virtual machines will have the same  type of disk as the source vApp. |
| thin | Each disk in the cloned virtual machines is allocated in full  size now and committed on demand. This is only supported on  VMFS-3 and newer datastores. Other types of datastores may  create thick disks. |
| thick | Each disk in the cloned virtual machines are allocated and  committed in full size immediately. |


<a name='vim.vApp.IPAssignmentInfo.AllocationSchemes'>VAppIPAssignmentInfoAllocationSchemes</a> - vim.vApp.IPAssignmentInfo
===========================================================================================================================
IP allocation schemes supported by the guest.
| name | description |
|:-----|:------------|
| dhcp | The vApp supports DHCP to acquire IP configuration. |
| ovfenv | The vApp supports setting the IP configuration through the  properties provided in the OVF environment. |


<a name='vim.vApp.IPAssignmentInfo.IpAllocationPolicy'>VAppIPAssignmentInfoIpAllocationPolicy</a> - vim.vApp.IPAssignmentInfo
=============================================================================================================================
IP allocation policy for a deployment.
| name | description |
|:-----|:------------|
| dhcpPolicy | Specifies that DHCP must be used to allocate IP addresses to the vApp |
| transientPolicy | Specifies that IP allocation is done through the range managed by the   vSphere platform. The IP addresses are allocated when needed, typically at   power-on, and deallocated during power-off. There is no guarantee that a   vApp will get the same IP address when restarted. |
| fixedPolicy | Specifies that IP addresses are configured manually when the vApp is deployed   and will be kept until reconfigured or the vApp destroyed. This will ensure   that a vApp gets a consistent IP for its life-time. |
| fixedAllocatedPolicy | Specifies that IP allocation is done through the range managed by the VI   platform. The IP addresses are allocated at first power-on, and remain   allocated at power-off. This will ensure that a vApp gets a consistent  IP for its life-time. |


<a name='vim.vApp.IPAssignmentInfo.Protocols'>VAppIPAssignmentInfoProtocols</a> - vim.vApp.IPAssignmentInfo
===========================================================================================================
IP protocols supported by the guest.
| name | description |
|:-----|:------------|
| IPv4 | The vApp supports IPv4 protocol. |
| IPv6 | The vApp supports IPv6 protocol. |


<a name='vim.fault.VFlashModuleNotSupported.Reason'>VFlashModuleNotSupportedReason</a> - vim.fault.VFlashModuleNotSupported
===========================================================================================================================
| name | description |
|:-----|:------------|
| CacheModeNotSupported | CacheModeNotSupported |
| CacheConsistencyTypeNotSupported | CacheConsistencyTypeNotSupported |
| CacheBlockSizeNotSupported | CacheBlockSizeNotSupported |
| CacheReservationNotSupported | CacheReservationNotSupported |
| DiskSizeNotSupported | DiskSizeNotSupported |


<a name='vim.ServiceInstance.VMotionCompatibilityType'>VMotionCompatibilityType</a> - vim.ServiceInstance
=========================================================================================================
Types of a host's compatibility with a designated virtual machine   that is a candidate for VMotion. Used with queryVMotionCompatibility   both as inputs (to designate which compatibility types to test for)   and as outputs (to specify which compatibility types apply for   each host).
| name | description |
|:-----|:------------|
| cpu | The host's CPU features are compatible with the   the virtual machine's requirements. |
| software | The software platform on the host supports VMotion   and is compatible with the virtual machine. |


<a name='vim.dvs.VmwareDistributedVirtualSwitch.TeamingMatchStatus'>VMwareDVSTeamingMatchStatus</a> - vim.dvs.VmwareDistributedVirtualSwitch
============================================================================================================================================
The teaming health check match status.
| name | description |
|:-----|:------------|
| iphashMatch | The value of 'loadbalance_ip' is used in a uplink teaming policy   <a href="vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy.md#policy">policy</a>   in the vSphere Distributed Switch, and the external physical switch   has the matching EtherChannel configuration. |
| nonIphashMatch | The value of 'loadbalance_ip' is not used in a uplink teaming policy   <a href="vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy.md#policy">policy</a>   in the vSphere Distributed Switch, and the external physical switch   does not have EtherChannel configuration. |
| iphashMismatch | The value of 'loadbalance_ip' is used in a uplink teaming policy   <a href="vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy.md#policy">policy</a>   in the vSphere Distributed Switch, but the external physical switch   does not have the matching EtherChannel configuration. |
| nonIphashMismatch | The value of 'loadbalance_ip' is not used in a uplink teaming policy   <a href="vim.dvs.VmwareDistributedVirtualSwitch.UplinkPortTeamingPolicy.md#policy">policy</a>   in the vSphere Distributed Switch, but the external physical switch   has EtherChannel configuration. |


<a name='vim.dvs.VmwareDistributedVirtualSwitch.VspanSessionType'>VMwareDVSVspanSessionType</a> - vim.dvs.VmwareDistributedVirtualSwitch
========================================================================================================================================
Distributed Port Mirroring session types.
| name | description |
|:-----|:------------|
| mixedDestMirror | In mixedDestMirror session, Distributed Ports can be used as source entities,   and both Distributed Ports and Uplink Ports Name can be used as destination entities. |
| dvPortMirror | In dvPortMirror session, Distributed Ports can be used as both source   and destination entities. |
| remoteMirrorSource | In remoteMirrorSource session, Distributed Ports can be used as source entities,   and uplink ports name can be used as destination entities. |
| remoteMirrorDest | In remoteMirrorDest session, vlan Ids can be used as source entities,   and Distributed Ports can be used as destination entities. |
| encapsulatedRemoteMirrorSource | In encapsulatedRemoteMirrorSource session, Distributed Ports can be used as source entities,   and Ip address can be used as destination entities. |


<a name='vim.dvs.VmwareDistributedVirtualSwitch.LacpApiVersion'>VMwareDvsLacpApiVersion</a> - vim.dvs.VmwareDistributedVirtualSwitch
====================================================================================================================================
Link Aggregation Control Protocol API versions.
| name | description |
|:-----|:------------|
| singleLag | One Link Aggregation Control Protocol group in the switch |
| multipleLag | Multiple Link Aggregation Control Protocol in the switch. |


<a name='vim.dvs.VmwareDistributedVirtualSwitch.LacpLoadBalanceAlgorithm'>VMwareDvsLacpLoadBalanceAlgorithm</a> - vim.dvs.VmwareDistributedVirtualSwitch
========================================================================================================================================================
Load balance algorithm in a Link Aggregation Control Protocol group.
| name | description |
|:-----|:------------|
| srcMac | Source MAC address |
| destMac | Destination MAC address |
| srcDestMac | Source and destination MAC address |
| destIpVlan | Destination IP and VLAN |
| srcIpVlan | Source IP and VLAN |
| srcDestIpVlan | Source and destination IP and VLAN |
| destTcpUdpPort | Destination TCP/UDP port number |
| srcTcpUdpPort | Source TCP/UDP port number |
| srcDestTcpUdpPort | Source and destination TCP/UDP port number |
| destIpTcpUdpPort | Destination IP and TCP/UDP port number |
| srcIpTcpUdpPort | Source IP and TCP/UDP port number |
| srcDestIpTcpUdpPort | Source and destination IP and TCP/UDP port number |
| destIpTcpUdpPortVlan | Destination IP, TCP/UDP port number and VLAN |
| srcIpTcpUdpPortVlan | Source IP, TCP/UDP port number and VLAN |
| srcDestIpTcpUdpPortVlan | Source and destination IP,   source and destination TCP/UDP port number and VLAN. |
| destIp | Destination IP |
| srcIp | Source IP |
| srcDestIp | Source and Destination IP |
| vlan | VLAN only |
| srcPortId | Source Virtual Port Id |


<a name='vim.dvs.VmwareDistributedVirtualSwitch.UplinkLacpMode'>VMwareUplinkLacpMode</a> - vim.dvs.VmwareDistributedVirtualSwitch
=================================================================================================================================
Link Aggregation Control Protocol policy modes.
| name | description |
|:-----|:------------|
| active | Link Aggregation Control Protocol always sends frames along the configured uplinks |
| passive | Link Aggregation Control Protocol acts as "speak when spoken to". |


<a name='vim.ServiceInstance.ValidateMigrationTestType'>ValidateMigrationTestType</a> - vim.ServiceInstance
===========================================================================================================
Types of tests available for validateMigration.
| name | description |
|:-----|:------------|
| sourceTests | Tests that examine only the configuration   of the virtual machine and its current host; the destination   resource pool and host or cluster are irrelevant. |
| compatibilityTests | Tests that examine both the virtual   machine and the destination host or cluster; the destination   resource pool is irrelevant. This set excludes tests that fall   into the diskAccessibilityTests group. |
| diskAccessibilityTests | Tests that check that the   destination host or cluster can see the datastores where the virtual   machine's virtual disks are currently located. The destination   resource pool is irrelevant. If you are planning to relocate the   virtual disks, do not use these tests; instead examine the relevant   datastore objects for your planned disk locations to see if they   are accessible to the destination host. |
| resourceTests | Tests that check that the destination resource   pool can support the virtual machine if it is powered on. The   destination host or cluster is relevant because it will affect the   amount of overhead memory required to run the virtual machine. |


<a name='vim.VirtualApp.VAppState'>VirtualAppVAppState</a> - vim.VirtualApp
===========================================================================
The VAppState type defines the set of states a vApp can be   in. The transitory states between started and stopped is modeled explicitly,   since the starting or stopping of a vApp is typically a time-consuming   process that might take minutes to complete.
| name | description |
|:-----|:------------|
| started | The vApp is currently powered on . |
| stopped | The vApp is currently powered off or suspended. |
| starting | The vApp is in the process of starting. |
| stopping | The vApp is in the process of stopping. |


<a name='vim.vm.device.VirtualDeviceSpec.FileOperation'>VirtualDeviceConfigSpecFileOperation</a> - vim.vm.device.VirtualDeviceSpec
==================================================================================================================================
The type of operation being performed on the backing of a virtual device.   Valid values are:
| name | description |
|:-----|:------------|
| create | Specifies the creation of the device backing; for example,   the creation of a virtual disk or floppy image file. |
| destroy | Specifies the destruction of a device backing. |
| replace | Specifies the deletion of the existing backing for a virtual device   and the creation of a new backing. |


<a name='vim.vm.device.VirtualDeviceSpec.Operation'>VirtualDeviceConfigSpecOperation</a> - vim.vm.device.VirtualDeviceSpec
==========================================================================================================================
The type of operation being performed on the specified virtual device.   Valid values are:
| name | description |
|:-----|:------------|
| add | Specifies the addition of a virtual device to the configuration. |
| remove | Specifies the removal of a virtual device. |
| edit | Specifies changes to the virtual device specification. |


<a name='vim.vm.device.VirtualDevice.ConnectInfo.Status'>VirtualDeviceConnectInfoStatus</a> - vim.vm.device.VirtualDevice.ConnectInfo
=====================================================================================================================================
Specifies the connectable virtual device status.
| name | description |
|:-----|:------------|
| ok | The device is working correctly. |
| recoverableError | The device has reported a recoverable error. For example,   attempting to connect to floppy device that is being used by   another virtual machine or some other program would result in   this status. |
| unrecoverableError | The device cannot be used. For example, attempting to connect to   a floppy device that does not exist would result in this status. |
| untried | The device status is unknown, or it has not been requested to   connect when the VM is powered on. |


<a name='vim.vm.device.VirtualDeviceOption.FileBackingOption.FileExtension'>VirtualDeviceFileExtension</a> - vim.vm.device.VirtualDeviceOption.FileBackingOption
================================================================================================================================================================
All known file extensions. Valid ones are:
| name | description |
|:-----|:------------|
| iso | CD ISO Image backings |
| flp | Floppy File Backings |
| vmdk | virtual disks |
| dsk | legacy virtual disks |
| rdm | pre 3.0 virtual disks using Raw Disk Maps |


<a name='vim.vm.device.VirtualDeviceOption.URIBackingOption.Direction'>VirtualDeviceURIBackingOptionDirection</a> - vim.vm.device.VirtualDeviceOption.URIBackingOption
======================================================================================================================================================================
The <code>VirtualDeviceURIBackingOptionDirection</code> enum type    provides values for the direction of a network connection.
| name | description |
|:-----|:------------|
| server | Indicates that the virtual machine can listen for a connection   on the specified <a href="vim.vm.device.VirtualDevice.URIBackingInfo.md#serviceURI">serviceURI</a>. |
| client | Indicates that the virtual machine can initiate a connection   with a system on the network using the specified   <a href="vim.vm.device.VirtualDevice.URIBackingInfo.md#serviceURI">serviceURI</a>. |


<a name='vim.VirtualDiskManager.VirtualDiskAdapterType'>VirtualDiskAdapterType</a> - vim.VirtualDiskManager
===========================================================================================================
The types of virtual disk adapters used by virtual disks
| name | description |
|:-----|:------------|
| ide | Use IDE emulation for the virtual disk |
| busLogic | Use BusLogic emulation for the virtual disk |
| lsiLogic | Use LSILogic emulation for the virtual disk |


<a name='vim.vm.device.VirtualDiskOption.CompatibilityMode'>VirtualDiskCompatibilityMode</a> - vim.vm.device.VirtualDiskOption
==============================================================================================================================
All known compatibility modes for raw disk mappings. Valid compatibility   modes are:   <ul>   <li>virtualMode   <li>physicalMode   </ul>
| name | description |
|:-----|:------------|
| virtualMode | A disk device backed by a virtual compatibility mode raw disk mapping can   use disk modes.<br>See <a href="vim.vm.device.VirtualDiskOption.DiskMode.md">VirtualDiskMode</a><br> |
| physicalMode | A disk device backed by a physical compatibility mode raw disk mapping cannot   use disk modes, and commands are passed straight through to the LUN   indicated by the raw disk mapping. |


<a name='vim.vm.device.VirtualDisk.DeltaDiskFormat'>VirtualDiskDeltaDiskFormat</a> - vim.vm.device.VirtualDisk
==============================================================================================================
The delta disk format constants
| name | description |
|:-----|:------------|
| redoLogFormat | redo-log based format |
| nativeFormat | native snapshot format |
| seSparseFormat | Flex-SE redo-log based format |


<a name='vim.vm.device.VirtualDiskOption.DiskMode'>VirtualDiskMode</a> - vim.vm.device.VirtualDiskOption
========================================================================================================
The list of known disk modes.   <p>   The list of supported disk modes varies by the backing type. The "persistent"   mode is supported by every backing type.
| name | description |
|:-----|:------------|
| persistent | Changes are immediately and permanently written to the virtual disk. |
| nonpersistent | Changes to virtual disk are made to a redo log and discarded at power off. |
| undoable | Changes are made to a redo log, but you are given the option to commit or undo. |
| independent_persistent | Same as persistent, but not affected by snapshots. |
| independent_nonpersistent | Same as nonpersistent, but not affected by snapshots. |
| append | Changes are appended to the redo log; you revoke changes by removing the undo log. |


<a name='vim.VirtualDiskManager.VirtualDiskType'>VirtualDiskType</a> - vim.VirtualDiskManager
=============================================================================================
The types of virtual disks that can be created or cloned.
| name | description |
|:-----|:------------|
| preallocated | A preallocated disk has all space allocated at creation time  and the space is zeroed on demand as the space is used. |
| thin | Space required for thin-provisioned virtual disk is allocated and  zeroed on demand as the space is used. |
| seSparse | A sparse (allocate on demand) format with additional space  optimizations. |
| rdm | Virtual compatibility mode raw disk mapping.  An rdm virtual disk  grants access to the entire raw disk and the virtual disk can  participate in snapshots. |
| rdmp | Physical compatibility mode (pass-through) raw disk mapping. An rdmp  virtual disk passes SCSI commands directly to the hardware, but the  virtual disk cannot participate in snapshots. |
| raw | Raw device. |
| delta | A redo log disk. This format is only applicable as a destination format  in a clone operation, and not usable for disk creation. |
| sparse2Gb | A sparse disk with 2GB maximum extent size.  Disks in this format  can be used with other VMware products.  The 2GB extent size  makes these disks easier to burn to dvd or use on filesystems that  don't support large files. This format is only applicable as a  destination format in a clone operation, and not usable for disk  creation. |
| thick2Gb | A thick disk with 2GB maximum extent size.  Disks in this format  can be used with other VMware products.  The 2GB extent size  makes these disks easier to burn to dvd or use on filesystems that  don't support large files. This format is only applicable as a  destination format in a clone operation, and not usable for disk  creation. |
| eagerZeroedThick | An eager zeroed thick disk has all space allocated and wiped clean  of any previous contents on the physical media at creation time.  Such disks may take longer time during creation  compared to other  disk formats. |
| sparseMonolithic | A sparse monolithic disk.  Disks in this format can be used with other  VMware products. This format is only applicable as a destination  format in a clone operation, and not usable for disk creation. |
| flatMonolithic | A preallocated monolithic disk.  Disks in this format can be used with  other VMware products. This format is only applicable as a destination  format in a clone operation, and not usable for disk creation. |
| thick | A thick disk has all space allocated at creation time.  This  space may contain stale data on the physical media.  Thick disks  are primarily used for virtual machine clustering, but they are  generally insecure and should not be used. Due to better performance  and security properties, the use of the 'preallocated' format is  preferred over this format. |


<a name='vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheConsistencyType'>VirtualDiskVFlashCacheConfigInfoCacheConsistencyType</a> - vim.vm.device.VirtualDisk.VFlashCacheConfigInfo
=========================================================================================================================================================================================
Pre-defined constants for cache consistency types
| name | description |
|:-----|:------------|
| strong | With strong consistency, it ensures that  a crash will leave the cache data consistent. |
| weak | Cache data consistency is not guaranteed after a crash. |


<a name='vim.vm.device.VirtualDisk.VFlashCacheConfigInfo.CacheMode'>VirtualDiskVFlashCacheConfigInfoCacheMode</a> - vim.vm.device.VirtualDisk.VFlashCacheConfigInfo
===================================================================================================================================================================
Pre-defined constants for cache modes.
| name | description |
|:-----|:------------|
| write_thru | In write-through cache mode, writes to the cache cause writes  to the underlying storage. The cache acts as a facade to the underlying  storage. |
| write_back | In write-back mode, writes to the cache do not go to the underlying storage  right away. Cache holds data temporarily till it can be permanently saved or  otherwise modified. |


<a name='vim.vm.device.VirtualEthernetCardOption.LegacyNetworkBackingOption.LegacyNetworkDeviceName'>VirtualEthernetCardLegacyNetworkDeviceName</a> - vim.vm.device.VirtualEthernetCardOption.LegacyNetworkBackingOption
========================================================================================================================================================================================================================
Possible device names for legacy network backing option are listed below.  Note: This is not an exhaustive list. It is possible to specify  a specific device as well.  For example, on ESX hosts, the device name could be specified as "vmnic[0-9]"  or vmnet_[0-9].  For VMware Server Windows hosts, the device name could be specified as "vmnet[0-9]"  and for VMware Server Linux hosts, the device name could be specified as "/dev/vmnet[0-9]"  depending on what devices are available on that particular host.
| name | description |
|:-----|:------------|
| bridged | bridged |
| nat | nat |
| hostonly | hostonly |


<a name='vim.vm.device.VirtualEthernetCardOption.MacTypes'>VirtualEthernetCardMacType</a> - vim.vm.device.VirtualEthernetCardOption
===================================================================================================================================
The enumeration of all known valid MAC address types.
| name | description |
|:-----|:------------|
| manual | A statistically assigned MAC address. |
| generated | An automatically generated MAC address. |
| assigned | A MAC address assigned by VirtualCenter. |


<a name='vim.VirtualMachine.AppHeartbeatStatusType'>VirtualMachineAppHeartbeatStatusType</a> - vim.VirtualMachine
=================================================================================================================
Application heartbeat status type.
| name | description |
|:-----|:------------|
| appStatusGray | Heartbeat status is disabled |
| appStatusGreen | Heartbeat status is OK |
| appStatusRed | Heartbeating has stopped |


<a name='vim.vm.ConfigInfo.NpivWwnType'>VirtualMachineConfigInfoNpivWwnType</a> - vim.vm.ConfigInfo
===================================================================================================
The NPIV WWN source type.
| name | description |
|:-----|:------------|
| vc | This set of WWNs is generated by VC server. |
| host | This set of WWNs is generated by Host Agent. |
| external | This set of WWNs is provided by the client. |


<a name='vim.vm.ConfigInfo.SwapPlacementType'>VirtualMachineConfigInfoSwapPlacementType</a> - vim.vm.ConfigInfo
===============================================================================================================
Available choices for virtual machine swapfile placement policy. This is   the set of legal values for the virtual machine configuration's   <a href="vim.vm.ConfigInfo.md#swapPlacement">swapPlacement</a> property. All   values except for "inherit" and "vmConfigured" are also valid values for   a compute resource configuration's   <a href="vim.ComputeResource.ConfigInfo.md#vmSwapPlacement">vmSwapPlacement</a>   property.
| name | description |
|:-----|:------------|
| inherit | Honor the virtual machine swapfile placement policy of the compute   resource that contains this virtual machine. |
| vmDirectory | Store the swapfile in the same directory as the virtual machine. |
| hostLocal | Store the swapfile in the datastore specified by the   <a href="vim.host.ConfigInfo.md#localSwapDatastore">localSwapDatastore</a>   property of the virtual machine's host, if that property is set and   indicates a datastore with sufficient free space. Otherwise store the   swapfile in the same directory as the virtual machine.   <p>   Note: This setting may degrade VMotion performance. |


<a name='vim.vm.ConfigSpec.NpivWwnOp'>VirtualMachineConfigSpecNpivWwnOp</a> - vim.vm.ConfigSpec
===============================================================================================
The root WWN operation mode.
| name | description |
|:-----|:------------|
| generate | Generate a new set of WWNs and assign it to the virtual machine. |
| set | Take a client-specified set of WWNs (specified in "wwn" property) and   assign them to the virtual machine. If the new WWN quntity are more   than existing then we will append them to the existing list of WWNs. |
| remove | Remove the currently assigned WWNs from the virtual machine. |
| extend | Generate a new set of WWNs and append them to the existing list |


<a name='vim.VirtualMachine.ConnectionState'>VirtualMachineConnectionState</a> - vim.VirtualMachine
===================================================================================================
The connectivity state of a virtual machine. When the API is provided directly by  a server product, such as ESX Server, then the disconnected state is not  possible. However, when accessed through VirtualCenter, the state of a virtual  machine is set to disconnected if the hosts that manage the virtual  machine becomes unavailable.
| name | description |
|:-----|:------------|
| connected | The server has access to the virtual machine. |
| disconnected | The server is currently disconnected from the virtual machine, since its   host is disconnected. See general comment for this enumerated type for more   details. |
| orphaned | The virtual machine is no longer registered on the host it is associated   with. For example, a virtual machine that is unregistered or deleted   directly on a host managed by VirtualCenter shows up in this state. |
| inaccessible | One or more of the virtual machine configuration files are inaccessible. For   example, this can be due to transient disk failures. In this case, no   configuration can be returned for a virtual machine. |
| invalid | The virtual machine configuration format is invalid. Thus, it is accessible  on disk, but corrupted in a way that does not allow the server to read the  content. In this case, no configuration can be returned for a virtual  machine. |


<a name='vim.vm.DeviceRuntimeInfo.VirtualEthernetCardRuntimeState.VmDirectPathGen2InactiveReasonOther'>VirtualMachineDeviceRuntimeInfoVirtualEthernetCardRuntimeStateVmDirectPathGen2InactiveReasonOther</a> - vim.vm.DeviceRuntimeInfo.VirtualEthernetCardRuntimeState
=======================================================================================================================================================================================================================================================================
| name | description |
|:-----|:------------|
| vmNptIncompatibleHost | The virtual machine's host does not support VMDirectPath Gen 2.<br>See <a href="vim.host.Capability.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a><br> |
| vmNptIncompatibleNetwork | The configuration or state of the attached network prevents   VMDirectPath Gen 2. Refer to   <a href="vim.dvs.DistributedVirtualPort.RuntimeInfo.md#vmDirectPathGen2InactiveReasonNetwork">vmDirectPathGen2InactiveReasonNetwork</a>   and/or   <a href="vim.dvs.DistributedVirtualPort.RuntimeInfo.md#vmDirectPathGen2InactiveReasonExtended">vmDirectPathGen2InactiveReasonExtended</a>   in the RuntimeInfo of the DistributedVirtualPort connected to this   device. |


<a name='vim.vm.DeviceRuntimeInfo.VirtualEthernetCardRuntimeState.VmDirectPathGen2InactiveReasonVm'>VirtualMachineDeviceRuntimeInfoVirtualEthernetCardRuntimeStateVmDirectPathGen2InactiveReasonVm</a> - vim.vm.DeviceRuntimeInfo.VirtualEthernetCardRuntimeState
=================================================================================================================================================================================================================================================================
| name | description |
|:-----|:------------|
| vmNptIncompatibleGuest | The virtual machine's guest OS does not support   VMDirectPath Gen 2. |
| vmNptIncompatibleGuestDriver | The virtual machine's guest network driver does not support   VMDirectPath Gen 2. |
| vmNptIncompatibleAdapterType | The device type does not support VMDirectPath Gen 2.<br>See <a href="vim.vm.device.VirtualEthernetCardOption.md#vmDirectPathGen2Supported">vmDirectPathGen2Supported</a><br> |
| vmNptDisabledOrDisconnectedAdapter | The virtual machine's network adapter is disabled or   disconnected, and thus is not participating in VMDirectPath Gen 2. |
| vmNptIncompatibleAdapterFeatures | The virtual machine's network adapter has features enabled   which preclude it participating in VMDirectPath Gen 2 such    as INT-x or PXE booting. |
| vmNptIncompatibleBackingType | The device backing is not a DistributedVirtualPortBacking. |
| vmNptInsufficientMemoryReservation | The virtual machine does not have full memory reservation    required to activate VMDirectPath Gen 2. |
| vmNptFaultToleranceOrRecordReplayConfigured | The virtual machine is configured for Fault Tolerance or   Record & Replay, which prevents VMDirectPath Gen 2. |
| vmNptConflictingIOChainConfigured | Some networking feature has placed a conflicting IOChain on    the network adapter, which prevents VMDirectPath Gen 2.  Examples    include DVFilter. |
| vmNptMonitorBlocks | The virtual machine monitor is exercising functionality which   which prevents VMDirectPath Gen 2. |
| vmNptConflictingOperationInProgress | VMDirectPath Gen 2 is temporarily suspended while the virtual   machine executes an operation such as suspend. |
| vmNptRuntimeError | VMDirectPath Gen 2 is unavailable due to an unforeseen runtime error   in the virtualization platform (typically resource constraints.) |
| vmNptOutOfIntrVector | VMDirectPath Gen 2 is unavailable due to host run out of intr   vector in host. Guest can configure the vNIC to use less rx/tx   queues or use MSI instead of MSIX. |
| vmNptVMCIActive | VMDirectPath Gen 2 is unavailable due to Incompatibe feature   VMCI is active in the current VM. Kill the relevant VMCI   application(s) and restart the VM will allow the vNIC(s) to enter   passthrough mode. |


<a name='vim.VirtualMachine.FaultToleranceState'>VirtualMachineFaultToleranceState</a> - vim.VirtualMachine
===========================================================================================================
The FaultToleranceState type defines a simple set of states for a  fault tolerant virtual machine:  disabled, starting, and enabled.  <p>
| name | description |
|:-----|:------------|
| notConfigured | This state indicates that the virtual machine has not been  configured for fault tolerance. |
| disabled | For a virtual machine that is the primary in a fault tolerant group,  this state indicates that the virtual machine has at least one  registered secondary, but no secondary is enabled.   For a virtual machine that is the secondary in a fault tolerant  group, this state indicates that the secondary is disabled. |
| enabled | For a virtual machine that is the primary in a fault tolerant group,  this state indicates that the virtual machine is not currently  powered on, but has at least one enabled secondary   For a virtual machine that is the secondary in a fault tolerant  group, this state indicates that the secondary is enabled, but is  not currently powered on. |
| needSecondary | For a virtual machine that is the primary in a fault tolerant group,  this state indicates that the virtual machine is powered on and  has at least one enabled secondary, but no secondary is currenly  active.   This state is not valid for a virtual machine that is a secondary  in a fault tolerant group. |
| starting | For a virtual machine that is the primary in a fault tolerant group,  this state indicates that the virtual machine is powered on and has  at least one secondary that is synchronizing its state with the  primary.   For a virtual machine that is the secondary in a fault tolerant  group, this state indicates that the secondary is powered on and is  synchronizing its state with the primary virtual machine. |
| running | This state indicates that the virtual machine is running with fault  tolerance protection. |


<a name='vim.vm.FileLayoutEx.FileType'>VirtualMachineFileLayoutExFileType</a> - vim.vm.FileLayoutEx
===================================================================================================
File-type constants.
| name | description |
|:-----|:------------|
| config | Config (vmx) file. |
| extendedConfig | Extended config (vmxf) file. |
| diskDescriptor | Disk descriptor (vmdk) file. |
| diskExtent | Disk extent (-flat/-delta/-s/-rdm/-rdmp.vmdk) file. |
| digestDescriptor | Disk digest descriptor file. |
| digestExtent | Disk digest extent file. |
| diskReplicationState | Host based replicated disk persistent state (psf) file. |
| log | Log (log) file. |
| stat | Virtual machine statistics (stat) file. |
| namespaceData | Namespace data file. |
| nvram | Non-volatile RAM (nvram) file. |
| snapshotData | Snapshot data (vmsn) file. |
| snapshotList | Snapshot metadata (vmsd) file. |
| snapshotManifestList | Snapshot manifest metadata (-aux.xml) file.   <p>   This file is still being created but is no longer necessary since   the manifest metadata is now available in the snapshot metadata   (vmsd) file in vSphere 5.0. This type will be deprecated when   vSphere 4.1 is no longer supported. |
| suspend | Suspend (vmss) file. |
| swap | Swap (vswp/vmem) file. |
| uwswap | File generated by VMware ESX kernel for a running virtual  machine. |
| core | Core (core) file. |
| screenshot | Screenshot file. |


<a name='vim.vm.FlagInfo.MonitorType'>VirtualMachineFlagInfoMonitorType</a> - vim.vm.FlagInfo
=============================================================================================
Set of possible values for <a href="vim.vm.FlagInfo.md#monitorType">monitorType</a>.
| name | description |
|:-----|:------------|
| release | Run vmx in default mode, matching the build type of vmkernel. |
| debug | Run vmx in debug mode. |
| stats | Run vmx in stats mode. |


<a name='vim.vm.FlagInfo.VirtualExecUsage'>VirtualMachineFlagInfoVirtualExecUsage</a> - vim.vm.FlagInfo
=======================================================================================================
Set of possible values for <a href="vim.vm.FlagInfo.md#virtualExecUsage">virtualExecUsage</a>.
| name | description |
|:-----|:------------|
| hvAuto | Determine automatically whether to use hardware virtualization (HV) support. |
| hvOn | Use hardware virtualization (HV) support if the physical hardware supports it. |
| hvOff | Do not use hardware virtualization (HV) support. |


<a name='vim.vm.FlagInfo.VirtualMmuUsage'>VirtualMachineFlagInfoVirtualMmuUsage</a> - vim.vm.FlagInfo
=====================================================================================================
Set of possible values for <a href="vim.vm.FlagInfo.md#virtualMmuUsage">virtualMmuUsage</a>.
| name | description |
|:-----|:------------|
| automatic | Determine automatically whether to use nested page table hardware support. |
| on | Use nested paging hardware support if the physical hardware supports it. |
| off | Do not use nested page table hardware support. |


<a name='vim.vm.GuestOsDescriptor.GuestOsFamily'>VirtualMachineGuestOsFamily</a> - vim.vm.GuestOsDescriptor
===========================================================================================================
Guest operating system family constants.
| name | description |
|:-----|:------------|
| windowsGuest | Windows operating system |
| linuxGuest | Linux operating system |
| netwareGuest | Novell Netware |
| solarisGuest | Solaris operating system |
| darwinGuestFamily | Mac OS operating system |
| otherGuestFamily | Other operating systems |


<a name='vim.vm.GuestOsDescriptor.GuestOsIdentifier'>VirtualMachineGuestOsIdentifier</a> - vim.vm.GuestOsDescriptor
===================================================================================================================
Guest operating system identifier.
| name | description |
|:-----|:------------|
| dosGuest | MS-DOS. |
| win31Guest | Windows 3.1 |
| win95Guest | Windows 95 |
| win98Guest | Windows 98 |
| winMeGuest | Windows Millenium Edition |
| winNTGuest | Windows NT 4 |
| win2000ProGuest | Windows 2000 Professional |
| win2000ServGuest | Windows 2000 Server |
| win2000AdvServGuest | Windows 2000 Advanced Server |
| winXPHomeGuest | Windows XP Home Edition |
| winXPProGuest | Windows XP Professional |
| winXPPro64Guest | Windows XP Professional Edition (64 bit) |
| winNetWebGuest | Windows Server 2003, Web Edition |
| winNetStandardGuest | Windows Server 2003, Standard Edition |
| winNetEnterpriseGuest | Windows Server 2003, Enterprise Edition |
| winNetDatacenterGuest | Windows Server 2003, Datacenter Edition |
| winNetBusinessGuest | Windows Small Business Server 2003 |
| winNetStandard64Guest | Windows Server 2003, Standard Edition (64 bit) |
| winNetEnterprise64Guest | Windows Server 2003, Enterprise Edition (64 bit) |
| winLonghornGuest | Windows Longhorn (experimental) |
| winLonghorn64Guest | Windows Longhorn (64 bit) (experimental) |
| winNetDatacenter64Guest | Windows Server 2003, Datacenter Edition (64 bit) (experimental) |
| winVistaGuest | Windows Vista |
| winVista64Guest | Windows Vista (64 bit) |
| windows7Guest | Windows 7 |
| windows7_64Guest | Windows 7 (64 bit) |
| windows7Server64Guest | Windows Server 2008 R2 (64 bit) |
| windows8Guest | Windows 8 |
| windows8_64Guest | Windows 8 (64 bit) |
| windows8Server64Guest | Windows 8 Server (64 bit) |
| windowsHyperVGuest | Windows Hyper-V |
| freebsdGuest | FreeBSD |
| freebsd64Guest | FreeBSD x64 |
| redhatGuest | Red Hat Linux 2.1 |
| rhel2Guest | Red Hat Enterprise Linux 2 |
| rhel3Guest | Red Hat Enterprise Linux 3 |
| rhel3_64Guest | Red Hat Enterprise Linux 3 (64 bit) |
| rhel4Guest | Red Hat Enterprise Linux 4 |
| rhel4_64Guest | Red Hat Enterprise Linux 4 (64 bit) |
| rhel5Guest | Red Hat Enterprise Linux 5 |
| rhel5_64Guest | Red Hat Enterprise Linux 5 (64 bit) (experimental) |
| rhel6Guest | Red Hat Enterprise Linux 6 |
| rhel6_64Guest | Red Hat Enterprise Linux 6 (64 bit) |
| rhel7Guest | Red Hat Enterprise Linux 7 |
| rhel7_64Guest | Red Hat Enterprise Linux 7 (64 bit) |
| centosGuest | CentOS 4/5 |
| centos64Guest | CentOS 4/5 (64-bit) |
| oracleLinuxGuest | Oracle Linux 4/5 |
| oracleLinux64Guest | Oracle Linux 4/5 (64-bit) |
| suseGuest | Suse Linux |
| suse64Guest | Suse Linux (64 bit) |
| slesGuest | Suse Linux Enterprise Server 9 |
| sles64Guest | Suse Linux Enterprise Server 9 (64 bit) |
| sles10Guest | Suse linux Enterprise Server 10 |
| sles10_64Guest | Suse Linux Enterprise Server 10 (64 bit) (experimental) |
| sles11Guest | Suse linux Enterprise Server 11 |
| sles11_64Guest | Suse Linux Enterprise Server 11 (64 bit) |
| sles12Guest | Suse linux Enterprise Server 12 |
| sles12_64Guest | Suse Linux Enterprise Server 12 (64 bit) |
| nld9Guest | Novell Linux Desktop 9 |
| oesGuest | Open Enterprise Server |
| sjdsGuest | Sun Java Desktop System |
| mandrakeGuest | Mandrake Linux |
| mandrivaGuest | Mandriva Linux |
| mandriva64Guest | Mandriva Linux (64 bit) |
| turboLinuxGuest | Turbolinux |
| turboLinux64Guest | Turbolinux (64 bit) |
| ubuntuGuest | Ubuntu Linux |
| ubuntu64Guest | Ubuntu Linux (64 bit) |
| debian4Guest | Debian GNU/Linux 4 |
| debian4_64Guest | Debian GNU/Linux 4 (64 bit) |
| debian5Guest | Debian GNU/Linux 5 |
| debian5_64Guest | Debian GNU/Linux 5 (64 bit) |
| debian6Guest | Debian GNU/Linux 6 |
| debian6_64Guest | Debian GNU/Linux 6 (64 bit) |
| debian7Guest | Debian GNU/Linux 7 |
| debian7_64Guest | Debian GNU/Linux 7 (64 bit) |
| asianux3Guest | Asianux Server 3 |
| asianux3_64Guest | Asianux Server 3 (64 bit) |
| asianux4Guest | Asianux Server 4 |
| asianux4_64Guest | Asianux Server 4 (64 bit) |
| opensuseGuest | OpenSUSE Linux |
| opensuse64Guest | OpenSUSE Linux (64 bit) |
| fedoraGuest | Fedora Linux |
| fedora64Guest | Fedora Linux (64 bit) |
| other24xLinuxGuest | Linux 2.4x Kernel |
| other26xLinuxGuest | Linux 2.6x Kernel |
| otherLinuxGuest | Linux 2.2x Kernel |
| other3xLinuxGuest | Linux 3.x Kernel |
| genericLinuxGuest | Other Linux |
| other24xLinux64Guest | Linux 2.4x Kernel (64 bit) (experimental) |
| other26xLinux64Guest | Linux 2.6x Kernel (64 bit) (experimental) |
| other3xLinux64Guest | Linux 3.x Kernel (64 bit) |
| otherLinux64Guest | Linux (64 bit) (experimental) |
| solaris6Guest | Solaris 6 |
| solaris7Guest | Solaris 7 |
| solaris8Guest | Solaris 8 |
| solaris9Guest | Solaris 9 |
| solaris10Guest | Solaris 10 (32 bit) (experimental) |
| solaris10_64Guest | Solaris 10 (64 bit) (experimental) |
| solaris11_64Guest | Solaris 11 (64 bit) |
| os2Guest | OS/2 |
| eComStationGuest | eComStation 1.x |
| eComStation2Guest | eComStation 2.0 |
| netware4Guest | Novell NetWare 4 |
| netware5Guest | Novell NetWare 5.1 |
| netware6Guest | Novell NetWare 6.x |
| openServer5Guest | SCO OpenServer 5 |
| openServer6Guest | SCO OpenServer 6 |
| unixWare7Guest | SCO UnixWare 7 |
| darwinGuest | Mac OS 10.5 |
| darwin64Guest | Mac OS 10.5 (64 bit) |
| darwin10Guest | Mac OS 10.6 |
| darwin10_64Guest | Mac OS 10.6 (64 bit) |
| darwin11Guest | Mac OS 10.7 |
| darwin11_64Guest | Mac OS 10.7 (64 bit) |
| darwin12_64Guest | Mac OS 10.8 (64 bit) |
| darwin13_64Guest | Mac OS 10.9 (64 bit) |
| vmkernelGuest | VMware ESX 4 |
| vmkernel5Guest | VMware ESX 5 |
| otherGuest | Other Operating System |
| otherGuest64 | Other Operating System (64 bit) (experimental) |


<a name='vim.vm.GuestInfo.GuestState'>VirtualMachineGuestState</a> - vim.vm.GuestInfo
=====================================================================================
The possible hints that the guest could display about current tasks  inside the guest.
| name | description |
|:-----|:------------|
| running | running |
| shuttingDown | shuttingDown |
| resetting | resetting |
| standby | standby |
| notRunning | notRunning |
| unknown | unknown |


<a name='vim.vm.FlagInfo.HtSharing'>VirtualMachineHtSharing</a> - vim.vm.FlagInfo
=================================================================================
Set of possible values for <a href="vim.vm.FlagInfo.md#htSharing">htSharing</a>.
| name | description |
|:-----|:------------|
| any | VCPUs may freely share cores at any time with any other  VCPUs (default for all virtual machines on a hyperthreaded  system). |
| none | VCPUs should not share cores with each other or with VCPUs  from other virtual machines. That is, each VCPU from this  virtual machine should always get a whole core to itself,  with the other logical CPU on that core being placed into  the "halted" state. |
| internal | Similar to "none", in that VCPUs from this virtual machine  will not be allowed to share cores with VCPUs from other  virtual machines.  However, other VCPUs from the same virtual  machine will be allowed to share cores together. This  configuration option is only permitted for SMP virtual  machines. If applied to a uniprocessor virtual machine, it  will be converted to the "none" sharing option. |


<a name='vim.host.MemoryManagerSystem.VirtualMachineReservationInfo.AllocationPolicy'>VirtualMachineMemoryAllocationPolicy</a> - vim.host.MemoryManagerSystem.VirtualMachineReservationInfo
===========================================================================================================================================================================================
Means for allocating additional memory for virtual machines.
| name | description |
|:-----|:------------|
| swapNone | Fit all virtual machine memory into reserved host memory. |
| swapSome | Allow some virtual machine memory to be swapped. |
| swapMost | Allow most virtual machine memory to be swapped. |


<a name='vim.vm.MetadataManager.VmMetadataOp'>VirtualMachineMetadataManagerVmMetadataOp</a> - vim.vm.MetadataManager
====================================================================================================================
This enum represents the set of legal operations
| name | description |
|:-----|:------------|
| Update | Create or update the Metadata for the specified VM |
| Remove | Remove the Metadata for the specified VM |


<a name='vim.vm.MetadataManager.VmMetadataOwner.Owner'>VirtualMachineMetadataManagerVmMetadataOwnerOwner</a> - vim.vm.MetadataManager.VmMetadataOwner
=====================================================================================================================================================
This enum contains a list of valid owner values for   the name field
| name | description |
|:-----|:------------|
| ComVmwareVsphereHA | ComVmwareVsphereHA |


<a name='vim.VirtualMachine.MovePriority'>VirtualMachineMovePriority</a> - vim.VirtualMachine
=============================================================================================
MovePriority is an enumeration of values that indicate the priority of the task  that moves a virtual machine from one host to another or one storage location  to another. Note this priority can affect both the source and target hosts.
| name | description |
|:-----|:------------|
| lowPriority | The task of moving this virtual machine is low priority. |
| highPriority | The task of moving this virtual machine is high priority. |
| defaultPriority | The task of moving this virtual machine is the default priority. |


<a name='vim.VirtualMachine.NeedSecondaryReason'>VirtualMachineNeedSecondaryReason</a> - vim.VirtualMachine
===========================================================================================================
The NeedSecondaryReason type defines all reasons a virtual machine is  in the needSecondary Fault Tolerance state following a failure.
| name | description |
|:-----|:------------|
| initializing | Initializing FT |
| divergence | Divergence |
| lostConnection | Lose connection to secondary |
| partialHardwareFailure | Partial hardware failure |
| userAction | Terminated by user |
| other | All other reasons |


<a name='vim.vm.FlagInfo.PowerOffBehavior'>VirtualMachinePowerOffBehavior</a> - vim.vm.FlagInfo
===============================================================================================
Set of possible values for <a href="vim.vm.FlagInfo.md#snapshotPowerOffBehavior">snapshotPowerOffBehavior</a>.
| name | description |
|:-----|:------------|
| powerOff | Just power off the virtual machine. |
| revert | Revert to the snapshot. |
| prompt | Prompt the user for instructions at power-off time. |


<a name='vim.vm.DefaultPowerOpInfo.PowerOpType'>VirtualMachinePowerOpType</a> - vim.vm.DefaultPowerOpInfo
=========================================================================================================
The list of possible default power operations available for the virtual machine
| name | description |
|:-----|:------------|
| soft | soft |
| hard | hard |
| preset | preset |


<a name='vim.VirtualMachine.PowerState'>VirtualMachinePowerState</a> - vim.VirtualMachine
=========================================================================================
The PowerState type defines a simple set of states for a virtual machine:  poweredOn, poweredOff, and suspended. This type does not model substates,  such as when a task is running to change the virtual machine state.  If the virtual machine is in a state with a task in progress, it  transitions to a new state when the task completes. For example, a virtual  machine continues to be in the poweredOn state while a suspend task  is running, and changes to the suspended state once the task finishes.  <p>  As a consequence of this approach, clients interested in monitoring  the status of a virtual machine should typically track the  <a href="vim.ManagedEntity.md#recentTask">activeTask</a> data object in addition to the  <a href="vim.vm.RuntimeInfo.md#powerState">powerState</a> object.
| name | description |
|:-----|:------------|
| poweredOff | The virtual machine is currently powered off. |
| poweredOn | The virtual machine is currently powered on. |
| suspended | The virtual machine is currently suspended. |


<a name='vim.VirtualMachine.RecordReplayState'>VirtualMachineRecordReplayState</a> - vim.VirtualMachine
=======================================================================================================
The RecordReplayState type defines a simple set of record and replay  states for a virtual machine.
| name | description |
|:-----|:------------|
| recording | The virtual machine is recording. |
| replaying | The virtual machine is replaying. |
| inactive | The virtual machine is currently not participating  in record or replay. |


<a name='vim.vm.RelocateSpec.DiskMoveOptions'>VirtualMachineRelocateDiskMoveOptions</a> - vim.vm.RelocateSpec
=============================================================================================================
Specifies how a virtual disk is moved or copied to a   datastore.   <p>   In all cases after the move or copy the virtual machine's current running point   will be placed on the target datastore.  The current running point is defined   as the disk backing which the virtual machine is currently   writing to.  This end state can be achieved in multiple   ways, and the supported options are described in this   enumeration.   <p>   These options are only relevant when the backing of the   specified disk is a <a href="vim.vm.device.VirtualDevice.FileBackingInfo.md">file backing</a>.   <p>   Since disk backings may become shared as the result of   either a <a href="vim.VirtualMachine.md#clone">clone operation</a> or   a <a href="vim.VirtualMachine.md#relocate">relocate operation</a>,   <a href="vim.VirtualMachine.md#promoteDisks">PromoteDisks_Task</a> has been provided as   a way to unshare such disk backings.   <p><br>See <a href="vim.vm.device.VirtualDisk.SparseVer1BackingInfo.md#parent">parent</a><br>See <a href="vim.vm.device.VirtualDisk.SparseVer2BackingInfo.md#parent">parent</a><br>See <a href="vim.vm.device.VirtualDisk.FlatVer1BackingInfo.md#parent">parent</a><br>See <a href="vim.vm.device.VirtualDisk.FlatVer2BackingInfo.md#parent">parent</a><br>See <a href="vim.vm.device.VirtualDisk.RawDiskMappingVer1BackingInfo.md#parent">parent</a><br>See <a href="vim.vm.RelocateSpec.md#diskMoveType">diskMoveType</a><br>See <a href="vim.vm.RelocateSpec.DiskLocator.md#diskMoveType">diskMoveType</a><br>
| name | description |
|:-----|:------------|
| moveAllDiskBackingsAndAllowSharing | All of the virtual disk's backings should be moved to the new datastore.   <p>   If a disk backing is not the child-most backing of this virtual machine,   and there exists a read-only disk backing with the same content ID   on the target datastore, then this disk backing may not be copied.  Instead   it is acceptable to attach to the read-only disk backing at the target   datastore.  A read-only disk backing is defined as a virtual disk   backing which no virtual machine is currently writing to.   <p><br>See <a href="vim.vm.device.VirtualDisk.SparseVer1BackingInfo.md#contentId">contentId</a><br>See <a href="vim.vm.device.VirtualDisk.SparseVer2BackingInfo.md#contentId">contentId</a><br>See <a href="vim.vm.device.VirtualDisk.FlatVer1BackingInfo.md#contentId">contentId</a><br>See <a href="vim.vm.device.VirtualDisk.FlatVer2BackingInfo.md#contentId">contentId</a><br>See <a href="vim.vm.device.VirtualDisk.RawDiskMappingVer1BackingInfo.md#contentId">contentId</a><br> |
| moveAllDiskBackingsAndDisallowSharing | All of the virtual disk's backings should be moved to the new datastore.    It is not acceptable to attach to a disk backing with the same content ID   on the destination datastore.  During a <a href="vim.VirtualMachine.md#clone">clone operation</a> any delta disk backings will be consolidated. |
| moveChildMostDiskBacking | Move only the child-most disk backing.  Any parent disk backings should   be left in their current locations.   <p>   This option only differs from <a href="vim.vm.RelocateSpec.DiskMoveOptions.md#moveAllDiskBackingsAndAllowSharing">moveAllDiskBackingsAndAllowSharing</a> and   <a href="vim.vm.RelocateSpec.DiskMoveOptions.md#moveAllDiskBackingsAndDisallowSharing">moveAllDiskBackingsAndDisallowSharing</a> when the virtual   disk has a parent backing.   <p>   Note that in the case of a <a href="vim.VirtualMachine.md#clone">clone operation</a>,   this means that the parent disks will now be shared.  This is safe as any   parent disks are always read-only.    Note that in the case of a <a href="vim.VirtualMachine.md#relocate">RelocateVM_Task</a> operation,   only the virtual disks in the current virtual machine configuration are moved. |
| createNewChildDiskBacking | Create a new child disk backing on the destination datastore.  None of the   virtual disk's existing files should be moved from their current locations.   <p>   Note that in the case of a <a href="vim.VirtualMachine.md#clone">clone operation</a>,   this means that the original virtual machine's disks are now all being shared.   This is only safe if the clone was taken from a snapshot point, because   snapshot points are always read-only.  Thus for a clone this   option is only valid <a href="vim.vm.CloneSpec.md#snapshot">when cloning from a snapshot</a>.    Note that in the case of a <a href="vim.VirtualMachine.md#relocate">RelocateVM_Task</a> operation,   child disks are created for the virtual disks in the current virtual machine   configuration only. |
| moveAllDiskBackingsAndConsolidate | All of the virtual disk's backings should be moved to the new datastore.    During a <a href="vim.VirtualMachine.md#clone">clone operation</a> or a   <a href="vim.VirtualMachine.md#migrate">MigrateVM_Task</a>, any delta disk backings will be   consolidated. |


<a name='vim.vm.RelocateSpec.Transformation'>VirtualMachineRelocateTransformation</a> - vim.vm.RelocateSpec
===========================================================================================================
The set of tranformations that can be performed on the virtual disks  as part of the copy.
| name | description |
|:-----|:------------|
| flat | flat |
| sparse | sparse |


<a name='vim.vm.ScsiPassthroughInfo.ScsiClass'>VirtualMachineScsiPassthroughType</a> - vim.vm.ScsiPassthroughInfo
=================================================================================================================
Possible SCSI classes.
| name | description |
|:-----|:------------|
| disk | disk |
| tape | tape |
| printer | printer |
| processor | processor |
| worm | worm |
| cdrom | cdrom |
| scanner | scanner |
| optical | optical |
| media | media |
| com | com |
| raid | raid |
| unknown | unknown |


<a name='vim.vm.DefaultPowerOpInfo.StandbyActionType'>VirtualMachineStandbyActionType</a> - vim.vm.DefaultPowerOpInfo
=====================================================================================================================
The list of possible standby actions that the virtual machine can take   for S1 ACPI.
| name | description |
|:-----|:------------|
| checkpoint | checkpoint |
| powerOnSuspend | powerOnSuspend |


<a name='vim.vm.TargetInfo.ConfigurationTag'>VirtualMachineTargetInfoConfigurationTag</a> - vim.vm.TargetInfo
=============================================================================================================
Describes how widely the endpoint is availabe in a cluster. Note that these   fields are not neccessarily mutual-exclusive.
| name | description |
|:-----|:------------|
| compliant | Indicates that this device is part of the cluster compliant   specification. |
| clusterWide | Indicates that this is available for all hosts in the cluster. |


<a name='vim.VirtualMachine.TicketType'>VirtualMachineTicketType</a> - vim.VirtualMachine
=========================================================================================
The virtual machine ticket type.
| name | description |
|:-----|:------------|
| mks | Remote mouse-keyboard-screen ticket. |
| device | Remote device ticket. |
| guestControl | Guest operation ticket. |


<a name='vim.vm.GuestInfo.ToolsRunningStatus'>VirtualMachineToolsRunningStatus</a> - vim.vm.GuestInfo
=====================================================================================================
Current running status of VMware Tools running in the guest   operating system.
| name | description |
|:-----|:------------|
| guestToolsNotRunning | VMware Tools is not running. |
| guestToolsRunning | VMware Tools is running. |
| guestToolsExecutingScripts | VMware Tools is starting. |


<a name='vim.vm.GuestInfo.ToolsStatus'>VirtualMachineToolsStatus</a> - vim.vm.GuestInfo
=======================================================================================
Current status of VMware Tools running in the guest operating system.
| name | description |
|:-----|:------------|
| toolsNotInstalled | VMware Tools has never been installed   or has not run in the virtual machine. |
| toolsNotRunning | VMware Tools is not running. |
| toolsOld | VMware Tools is running, but the version is not current. |
| toolsOk | VMware Tools is running and the version is current. |


<a name='vim.vm.GuestInfo.ToolsVersionStatus'>VirtualMachineToolsVersionStatus</a> - vim.vm.GuestInfo
=====================================================================================================
Current version status of VMware Tools installed in the guest operating   system.
| name | description |
|:-----|:------------|
| guestToolsNotInstalled | VMware Tools has never been installed. |
| guestToolsNeedUpgrade | VMware Tools is installed, but the version is not current. |
| guestToolsCurrent | VMware Tools is installed, and the version is current. |
| guestToolsUnmanaged | VMware Tools is installed, but it is not managed by VMWare. |
| guestToolsTooOld | VMware Tools is installed, but the version is too old. |
| guestToolsSupportedOld | VMware Tools is installed, supported, but a newer version is available. |
| guestToolsSupportedNew | VMware Tools is installed, supported, and newer  than the version available on the host. |
| guestToolsTooNew | VMware Tools is installed, and the version is known to be  too new to work correctly with this virtual machine. |
| guestToolsBlacklisted | VMware Tools is installed, but the installed version is  known to have a grave bug and should be immediately upgraded. |


<a name='vim.vm.UsbInfo.Family'>VirtualMachineUsbInfoFamily</a> - vim.vm.UsbInfo
================================================================================
Device class family.
| name | description |
|:-----|:------------|
| audio | Audio capable device. |
| hid | Human interface device. |
| hid_bootable | Bootable human interface device, this is a subset of HID devices. |
| physical | Physical interface device. |
| communication | Communication device. |
| imaging | Still imaging device. |
| printer | Printer device. |
| storage | Mass storage device. |
| hub | USB hubs. |
| smart_card | Smart card device. |
| security | Content security device. |
| video | Video device. |
| wireless | Wireless controller. |
| bluetooth | Standard bluetooth adapter that uses HCI protocol,    this is a subset of wireless controllers. |
| wusb | Wireless device related to the Wireless USB standard,    this is a subset of wireless controllers, |
| pda | Palm PDA, and Micorsoft ActiveSync PDA. |
| vendor_specific | Device that has an interface using a vendor-specific protocol. |
| other | Other miscellaneous device. |
| unknownFamily | There was an error in determining this device's classes  accurately. |


<a name='vim.vm.UsbInfo.Speed'>VirtualMachineUsbInfoSpeed</a> - vim.vm.UsbInfo
==============================================================================
Device speed.
| name | description |
|:-----|:------------|
| low | This device operates at low speed (1.5Mb/s). |
| full | This device operates at full speed (12Mb/s). |
| high | This device can operate at high speed (480Mb/s) |
| superSpeed | This device can operate at super speed (4.8Gb/s) |
| unknownSpeed | This device's speed is unknown. |


<a name='vim.vm.device.VirtualVideoCard.Use3dRenderer'>VirtualMachineVideoCardUse3dRenderer</a> - vim.vm.device.VirtualVideoCard
================================================================================================================================
Set of possible values for <a href="vim.vm.device.VirtualVideoCard.md#use3dRenderer">use3dRenderer</a>.
| name | description |
|:-----|:------------|
| automatic | Determine automatically whether to render 3D with software or hardware. |
| software | Render 3D with software. |
| hardware | Render 3D with graphics hardware. |


<a name='vim.vm.device.VirtualPointingDeviceOption.DeviceBackingOption.HostPointingDeviceChoice'>VirtualPointingDeviceHostChoice</a> - vim.vm.device.VirtualPointingDeviceOption.DeviceBackingOption
====================================================================================================================================================================================================
The valid choices for host pointing devices are:    <p>
| name | description |
|:-----|:------------|
| autodetect | Automatically detects the host mouse type. |
| intellimouseExplorer | The Microsoft IntelliMouse Explorer. |
| intellimousePs2 | The Microsoft Intellimouse with a PS2 connection. |
| logitechMouseman | The Logitech MouseMan. |
| microsoft_serial | The Microsoft Serial Mouse. |
| mouseSystems | The Mouse Systems Mouse. |
| mousemanSerial | The Logitech MouseMan Serial Bus Mouse. |
| ps2 | A generic mouse with a PS2 connection. |


<a name='vim.vm.device.VirtualSCSIController.Sharing'>VirtualSCSISharing</a> - vim.vm.device.VirtualSCSIController
==================================================================================================================
Sharing describes three possible ways of sharing the SCSI bus:    One of these values is assigned to the sharedBus object to determine    if or how the SCSI bus is shared.
| name | description |
|:-----|:------------|
| noSharing | The virtual SCSI bus is not shared. |
| virtualSharing | The virtual SCSI bus is shared between two or more virtual machines.   In this case, no physical machine is involved. |
| physicalSharing | The virtual SCSI bus is shared between two or more virtual machines   residing on different physical hosts. |


<a name='vim.vm.device.VirtualSerialPortOption.EndPoint'>VirtualSerialPortEndPoint</a> - vim.vm.device.VirtualSerialPortOption
==============================================================================================================================
The <code><a href="vim.vm.device.VirtualSerialPortOption.EndPoint.md">VirtualSerialPortEndPoint</a> enum defines   endpoint values for virtual serial port pipe backing.   When you use serial port pipe backing to connect a virtual machine   to another process, you must define the endpoints.   See the <code><a href="vim.vm.device.VirtualSerialPort.PipeBackingInfo.md#endpoint">endpoint</a></code>   property for the virtual serial port pipe backing information data object.   <p>   The possible endpoint values are:   <ul>   <li>client   <li>server   </ul>   <p>   For the supported choices, see the   <code><a href="vim.vm.device.VirtualSerialPortOption.PipeBackingOption.md#endpoint">endpoint</a></code>   property for the virtual serial port pipe backing option data object.
| name | description |
|:-----|:------------|
| client | client |
| server | server |


<a name='vim.event.VmDasBeingResetEvent.ReasonCode'>VmDasBeingResetEventReasonCode</a> - vim.event.VmDasBeingResetEvent
=======================================================================================================================
| name | description |
|:-----|:------------|
| vmtoolsHeartbeatFailure | vmtools heartbeat failure |
| appHeartbeatFailure | application heartbeat failure |
| appImmediateResetRequest | immediate reset request |


<a name='vim.event.VmFailedStartingSecondaryEvent.FailureReason'>VmFailedStartingSecondaryEventFailureReason</a> - vim.event.VmFailedStartingSecondaryEvent
===========================================================================================================================================================
The reason for the failure.
| name | description |
|:-----|:------------|
| incompatibleHost | Remote host is incompatible for secondary virtual machine.  For instance, the host doesn't have access to the virtual machine's  network or datastore. |
| loginFailed | Login to remote host failed. |
| registerVmFailed | Registration of the secondary virtual machine  on the remote host failed. |
| migrateFailed | Migration failed. |


<a name='vim.fault.VmFaultToleranceConfigIssue.ReasonForIssue'>VmFaultToleranceConfigIssueReasonForIssue</a> - vim.fault.VmFaultToleranceConfigIssue
====================================================================================================================================================
| name | description |
|:-----|:------------|
| haNotEnabled | HA is not enabled on the cluster |
| moreThanOneSecondary | There is already a secondary virtual machine for the primary   virtual machine |
| recordReplayNotSupported | The virtual machine does not support record/replay.    Vm::Capability.RecordReplaySupported is false. |
| replayNotSupported | It is not possible to turn on Fault Tolerance on this powered-on VM.   The support for record/replay should be enabled or Fault Tolerance    turned on, when this VM is powered off. |
| templateVm | The virtual machine is a template |
| multipleVCPU | The virtual machine has more than one virtual CPU |
| hostInactive | The host is not active |
| ftUnsupportedHardware | The host ftSupported flag is not set because of hardware issues |
| ftUnsupportedProduct | The host ftSupported flag is not set because of it is a   VMware Server 2.0 |
| missingVMotionNic | No VMotion license or VMotion nic is not configured on the host |
| missingFTLoggingNic | FT logging nic is not configured on the host |
| thinDisk | The virtual machine has thin provisioned disks |
| verifySSLCertificateFlagNotSet | The "check host certificate" flag is not set |
| hasSnapshots | The virtual machine has one or more snapshots |
| noConfig | No configuration information is available for the virtual machine |
| ftSecondaryVm | The virtual machine is a fault tolerance secondary virtual machine |
| hasLocalDisk | The virtual machine has one or more disks on local datastore |
| esxAgentVm | The virtual machine is an ESX agent VM |
| video3dEnabled | The virtual machine video device has 3D enabled |
| hasUnsupportedDisk | hasUnsupportedDisk |
| hasNestedHVConfiguration | Nested HV and FT are mutually exclusive. Disallow turning on FT   when nested HV configuration is enabled on VM. |
| hasVFlashConfiguration | The virtual machine has a vFlash memory device or/and disks with   vFlash cache configured. |


<a name='vim.fault.VmFaultToleranceInvalidFileBacking.DeviceType'>VmFaultToleranceInvalidFileBackingDeviceType</a> - vim.fault.VmFaultToleranceInvalidFileBacking
=================================================================================================================================================================
| name | description |
|:-----|:------------|
| virtualFloppy | virtual floppy |
| virtualCdrom | virtual Cdrom |
| virtualSerialPort | virtual serial port |
| virtualParallelPort | virtual parallel port |
| virtualDisk | virtual disk |


<a name='vim.event.VmShutdownOnIsolationEvent.Operation'>VmShutdownOnIsolationEventOperation</a> - vim.event.VmShutdownOnIsolationEvent
=======================================================================================================================================
| name | description |
|:-----|:------------|
| shutdown | The virtual machine was shut down |
| poweredOff | The virtual machine was powered off because shut down failed |


<a name='vim.dvs.VmwareDistributedVirtualSwitch.PvlanPortType'>VmwareDistributedVirtualSwitchPvlanPortType</a> - vim.dvs.VmwareDistributedVirtualSwitch
=======================================================================================================================================================
The PVLAN port types.
| name | description |
|:-----|:------------|
| promiscuous | The port can communicate with all other ports within the same PVLAN,   including the isolated and community ports . |
| isolated | The port can only communicate with the promiscuous ports within the   same PVLAN, any other traffics are blocked. |
| community | The ports communicates with other community ports and with   promiscuous ports within the same PVLAN. any other traffics are   blocked. |


<a name='vim.vsan.host.VsanRuntimeInfo.DiskIssueType'>VsanDiskIssueType</a> - vim.vsan.host.VsanRuntimeInfo
===========================================================================================================
The list of disk issues.
| name | description |
|:-----|:------------|
| nonExist | nonExist |
| stampMismatch | stampMismatch |
| unknown | unknown |


<a name='vim.vsan.host.DecommissionMode.ObjectAction'>VsanHostDecommissionModeObjectAction</a> - vim.vsan.host.DecommissionMode
===============================================================================================================================
The action to take with regard to storage objects upon decommissioning  a host from use with the VSAN service.
| name | description |
|:-----|:------------|
| noAction | No special action should take place regarding VSAN data. |
| ensureObjectAccessibility | VSAN data reconfiguration should be performed to ensure storage  object accessibility. |
| evacuateAllData | VSAN data evacuation should be performed such that all storage  object data is removed from the host. |


<a name='vim.vsan.host.DiskResult.State'>VsanHostDiskResultState</a> - vim.vsan.host.DiskResult
===============================================================================================
Values used for indicating a disk's status for use by the VSAN service.<br>See <a href="vim.vsan.host.DiskResult.md#state">state</a><br>
| name | description |
|:-----|:------------|
| inUse | Disk is currently in use by the VSAN service.   A disk may be considered in use by the VSAN service regardless of  whether the VSAN service is enabled.  As long as a disk is in use  by VSAN, it is reserved exclusively for VSAN and may not be used  for other purposes.<br>See <a href="vim.vsan.host.DiskResult.md#error">error</a><br> |
| eligible | Disk is considered eligible for use by the VSAN service,  but is not currently in use. |
| ineligible | Disk is considered ineligible for use by the VSAN service,  and is not currently in use.<br>See <a href="vim.vsan.host.DiskResult.md#error">error</a><br> |


<a name='vim.vsan.host.HealthState'>VsanHostHealthState</a> - None
==================================================================
A <a href="vim.vsan.host.HealthState.md">VsanHostHealthState</a> represents the state of a participating  host in the VSAN service.<br>See <a href="vim.vsan.host.ClusterStatus.md">VsanHostClusterStatus</a><br>
| name | description |
|:-----|:------------|
| unknown | Node health is unknown. |
| healthy | Node is considered healthy. |
| unhealthy | Node is considered unhealthy. |


<a name='vim.vsan.host.NodeState'>VsanHostNodeState</a> - None
==============================================================
A <a href="vim.vsan.host.NodeState.md">VsanHostNodeState</a> represents the state of participation of a host  in the VSAN service.<br>See <a href="vim.vsan.host.ClusterStatus.md">VsanHostClusterStatus</a><br>See <a href="vim.vsan.host.ClusterStatus.State.md">VsanHostClusterStatusState</a><br>
| name | description |
|:-----|:------------|
| error | The node is enabled for the VSAN service but has some configuration  error which prevents participation. |
| disabled | The node is disabled for the VSAN service. |
| agent | The node is enabled for the VSAN service and is serving as an agent. |
| master | The node is enabled for the VSAN service and is serving as the master. |
| backup | The node is enabled for the VSAN service and is serving as the backup. |
| starting | The node is starting the VSAN service; this state is considered  transitory. |
| stopping | The node is stopping the VSAN service; this state is considered  transitory. |
| enteringMaintenanceMode | The node is entering maintenance mode; this state is considered  transitory.<br>See <a href="vim.HostSystem.md#enterMaintenanceMode">EnterMaintenanceMode_Task</a><br> |
| exitingMaintenanceMode | The node is exiting maintenance mode; this state is considered  transitory.<br>See <a href="vim.HostSystem.md#exitMaintenanceMode">ExitMaintenanceMode_Task</a><br> |
| decommissioning | The node is being decommissioned from the VSAN service; this state is  considered transitory. |


<a name='vim.scheduler.MonthlyByWeekdayTaskScheduler.WeekOfMonth'>WeekOfMonth</a> - vim.scheduler.MonthlyByWeekdayTaskScheduler
===============================================================================================================================
| name | description |
|:-----|:------------|
| first | first |
| second | second |
| third | third |
| fourth | fourth |
| last | last |


<a name='vim.fault.WillLoseHAProtection.Resolution'>WillLoseHAProtectionResolution</a> - vim.fault.WillLoseHAProtection
=======================================================================================================================
| name | description |
|:-----|:------------|
| svmotion | storage vmotion resolution |
| relocate | relocate resolution |
