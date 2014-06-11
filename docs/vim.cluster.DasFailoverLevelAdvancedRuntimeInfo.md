vim.cluster.DasFailoverLevelAdvancedRuntimeInfo
===============================================
inherits from [vim.cluster.DasAdvancedRuntimeInfo](docs/vim.cluster.DasAdvancedRuntimeInfo.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Advanced runtime information related to the high availability service  for a cluster that has been configured with a failover level admission control  policy. See <a href="vim.cluster.FailoverLevelAdmissionControlPolicy.md">ClusterFailoverLevelAdmissionControlPolicy</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| slotInfo | [vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.SlotInfo](vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.SlotInfo.md "vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.SlotInfo") | None | None | Slot information for this cluster. |
| totalSlots | int | None | None | The total number of slots available in the cluster.<br>See SlotInfo |
| usedSlots | int | None | None | The number of slots currently being used.<br>See SlotInfo |
| unreservedSlots | int | None | None | The number of slots that are not used by currently powered on virtual machines  and not reserved to satisfy the configured failover level. This number gives  an indication of how many additional virtual machines can be powered on in  this cluster without violating the failover level (assuming the new virtual  machine's reservations are satisfied by the current slot size).   This value is computed as follows (where m is the configured failover level):  Remove the m largest hosts (ie. the ones with the most slots) from the list  of "good" hosts (see <a href="vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.md#totalGoodHosts">totalGoodHosts</a>). Sum up the number of slots on  the remaining hosts and deduct the number of currently used slots  (see <a href="vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.md#usedSlots">usedSlots</a>). If this number is negative, use zero instead.<br>See SlotInfo |
| totalVms | int | None | None | The total number of powered on vms in the cluster. |
| totalHosts | int | None | None | The total number of hosts in the cluster. |
| totalGoodHosts | int | None | None | The total number of connected hosts that are not in maintance mode and that  do not have any DAS-related config issues on them. |
| hostSlots | [vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.HostSlots](vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.HostSlots.md "vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.HostSlots") | true | None |  |
| vmsRequiringMultipleSlots | [vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.VmSlots](vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.VmSlots.md "vim.cluster.DasFailoverLevelAdvancedRuntimeInfo.VmSlots") | true | None | The list of virtual machines whose reservations and memory overhead are not  satisfied by a single slot. |


