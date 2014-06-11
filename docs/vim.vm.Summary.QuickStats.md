vim.vm.Summary.QuickStats
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


A set of statistics that are typically updated with near real-time regularity.   This data object type does not support notification, for scalability reasons.   Therefore, changes in QuickStats do not generate property collector updates. To   monitor statistics values, use the statistics and alarms modules instead.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| overallCpuUsage | int | true | None | Basic CPU performance statistics, in MHz.   Valid while the virtual machine is running. |
| overallCpuDemand | int | true | None | Basic CPU performance statistics, in MHz.   Valid while the virtual machine is running. |
| guestMemoryUsage | int | true | None | Guest memory utilization statistics, in MB. This   is also known as active guest memory. The number   can be between 0 and the configured memory size of   the virtual machine. Valid while the virtual machine is   running. |
| hostMemoryUsage | int | true | None | Host memory utilization statistics, in MB. This   is also known as consumed host memory. This is between 0 and   the configured resource limit. Valid while the virtual machine is   running. This includes the overhead memory of the VM. |
| guestHeartbeatStatus | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | None | None | Guest operating system heartbeat metric.   See <a href="vim.VirtualMachine.md#guestHeartbeatStatus">guestHeartbeatStatus</a> for a description. |
| distributedCpuEntitlement | int | true | None | This is the amount of CPU resource, in MHz, that this VM is entitled to, as   calculated by DRS. Valid only for a VM managed by DRS. |
| distributedMemoryEntitlement | int | true | None | This is the amount of memory, in MB, that this VM is entitled to, as   calculated by DRS. Valid only for a VM managed by DRS. |
| staticCpuEntitlement | int | true | None | The static CPU resource entitlement for a virtual machine. This value is   calculated based on this virtual machine's resource reservations, shares   and limit, and doesn't take into account current usage. This is the worst   case CPU allocation for this virtual machine, that is, the amount of CPU   resource this virtual machine would receive if all virtual machines running   in the cluster went to maximum consumption. Units are MHz. |
| staticMemoryEntitlement | int | true | None | The static memory resource entitlement for a virtual machine. This value is   calculated based on this virtual machine's resource reservations, shares   and limit, and doesn't take into account current usage. This is the worst   case memory allocation for this virtual machine, that is, the amount of   memory this virtual machine would receive if all virtual machines running   in the cluster went to maximum consumption. Units are MB. |
| privateMemory | int | true | None | The portion of memory, in MB, that is granted to this VM from non-shared   host memory. |
| sharedMemory | int | true | None | The portion of memory, in MB, that is granted to this VM from host memory   that is shared between VMs. |
| swappedMemory | int | true | None | The portion of memory, in MB, that is granted to this VM from the host's swap   space. This is a sign that there is memory pressure on the host. |
| balloonedMemory | int | true | None | The size of the balloon driver in the VM, in MB. The host will inflate the   balloon driver to reclaim physical memory from the VM.  This is a sign that   there is memory pressure on the host. |
| consumedOverheadMemory | int | true | None | The amount of consumed overhead memory, in MB, for this VM. |
| ftLogBandwidth | int | true | None | The network bandwidth used for logging between the   primary and secondary fault tolerance VMs.   The unit is kilobytes per second. |
| ftSecondaryLatency | int | true | None | The amount of time in wallclock that the VCPU of the secondary fault   tolerance VM is behind the VCPU of the primary VM.   The unit is millisecond. |
| ftLatencyStatus | [vim.ManagedEntity.Status](vim.ManagedEntity.Status.md "vim.ManagedEntity.Status") | true | None | The latency status of the fault tolerance VM.   ftLatencyStatus is determined by the value of ftSecondaryLatency.   ftLatencyStatus is:      green,  if ftSecondaryLatency is less than or equal to 2 seconds;      yellow, if ftSecondaryLatency is greater than 2 seconds,              and less than or equal to 6 seconds;      red,    if ftSecondaryLatency is greater than 6 seconds;      gray,   if ftSecondaryLatency is unknown. |
| compressedMemory | long | true | None | The amount of compressed memory currently consumed by VM, in Kb. |
| uptimeSeconds | int | true | None | The system uptime of the VM in seconds. |
| ssdSwappedMemory | long | true | None | The amount of memory swapped to fast disk device such as  SSD, in KB. |


