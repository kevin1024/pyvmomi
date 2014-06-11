vim.alarm.AlarmDescription
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Static strings for alarms.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| expr | [vim.TypeDescription](vim.TypeDescription.md "vim.TypeDescription") | None | None | Descriptions of expression types for a trigger. |
| stateOperator | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.alarm.StateAlarmExpression.StateOperator.md">State Operator enum description</a> |
| metricOperator | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.alarm.MetricAlarmExpression.MetricOperator.md">MetricAlarmExpression Metric Operator enum description</a> |
| hostSystemConnectionState | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.HostSystem.ConnectionState.md">Host System Connection State enum description</a> |
| virtualMachinePowerState | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.VirtualMachine.PowerState.md">Virtual Machine Power State enum description</a> |
| datastoreConnectionState | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.Datastore.Summary.md#accessible">accessible</a> and   <a href="vim.host.MountInfo.md#accessible">description</a> |
| hostSystemPowerState | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.HostSystem.PowerState.md">Host System Power State enum description</a> |
| virtualMachineGuestHeartbeatStatus | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.ManagedEntity.Status.md">Guest Heartbeat Status enum description</a> |
| entityStatus | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | <a href="vim.ManagedEntity.Status.md">ManagedEntity Status enum description</a> |
| action | [vim.TypeDescription](vim.TypeDescription.md "vim.TypeDescription") | None | None | Action class descriptions for an alarm. |


