vim.cluster.DasFdmHostState
===========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


The <a href="vim.cluster.DasFdmHostState.md">ClusterDasFdmHostState</a> data object   describes the availability state of each active host in a   vSphere HA enabled cluster.   <p>   In a vSphere HA cluster, the active hosts form a fault domain.   A host is inactive if it is in standby or maintenance mode, or   it has been disconnected from vCenter Server. A vSphere HA   agent, called the Fault Domain Manager (FDM), runs on each host in the   fault domain.   <p>   One FDM serves as the master and the remaining FDMs as its slaves.   The master is responsible for monitoring the availability of the hosts   and VMs in the cluster, and restarting any VMs that fail due to a   host failure or non-user-initiated power offs. The master is also   responsible for reporting fault-domain state to vCenter Server.   <p>   The master FDM is determined through election by the FDMs that are   alive at the time. An election occurs in the following circumstances:   <ul>   <li> When the vSphere HA feature is enabled for the cluster.   <li> When the master's host fails.   <li> When the management network is partitioned. In a network partition   there will be a master for each partition. However, only one master   will be responsible for a given VM. When the partition is   resolved, all but one of the masters will abdicate.   <li> After a host in a vSphere HA cluster powers back up following a failure   that caused all hosts in the cluster to power off.   </ul>   <p>   The slaves are responsible for reporting state updates to the master and   restarting VMs as required. All FDMs provide the VM/Application Health   Monitoring Service.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| state | string | None | None | The Availability State of a host based on information   reported by the entity given by the   <a href="vim.cluster.DasFdmHostState.md#stateReporter">stateReporter</a> property. See   <a href="vim.cluster.DasFdmAvailabilityState.md">ClusterDasFdmAvailabilityState</a> for the set of   states. |
| stateReporter | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | true | None | The entity reporting the state of the host. If the reporter is a host,   the property reports which host, whereas if the reporter is vCenter Server,   the property is unset. |


