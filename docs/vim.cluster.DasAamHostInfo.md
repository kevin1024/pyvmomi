vim.cluster.DasAamHostInfo
==========================
inherits from [vim.cluster.DasHostInfo](docs/vim.cluster.DasHostInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)
### DEPRECATED



The <a href="vim.cluster.DasAamHostInfo.md">ClusterDasAamHostInfo</a> object contains a list of the ESX hosts   in an HA cluster and a list that identifies the <i>primary</i> hosts.   (AAM is a component of the HA service.)   The primary hosts share the joint responsibility of maintaining all cluster   state and one will initiate failover actions should a failure occur.   <p>   When you add an ESX host to a vSphere HA cluster, the host   downloads HA agent components from the vCenter Server.   The HA agent maintains communication with the vCenter Server.   <p>   When the host downloads the HA agent, the host configures the agent   to communicate with other agents in the cluster. A host that joins   the cluster communicates with an existing primary host to complete   its configuration (except when you are adding the first host to the cluster).   <ul>   <li>The first five hosts added to the cluster are designated   as primary hosts. All subsequent hosts are designated as secondary hosts.</li>   <li>If a primary host is removed from the cluster,   the vCenter Server promotes another host to primary status.</li>   <li>There must be at least one functional primary host for vSphere HA   to operate correctly. If there is not an available primary host   (no response), host configuration for HA will fail.   If there is a total cluster failure, HA will begin restarting virtual   machines as soon as one host recovers and its HA agent is up and running.</li>   </ul>   <p>   One of the primary hosts assumes the role of the active primary host.   The active primary host responsibilities include the following activities:   <ul>   <li>Decides where to restart virtual machines.</li>   <li>Tracks failed restart attempts.</li>   <li>Determines when it is appropriate to continue attempts to restart   a virtual machine.</li>   </ul>   <p>   If the active primary host fails, another primary host replaces it.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostDasState | [vim.cluster.DasAamNodeState](vim.cluster.DasAamNodeState.md "vim.cluster.DasAamNodeState") | true | None | The state of HA on the hosts. |
| primaryHosts | string | true | None | The list of primary hosts. |


