vim.event.ClusterStatusChangedEvent
===================================
inherits from [vim.event.ClusterEvent](docs/vim.event.ClusterEvent.md)


This event records when a cluster's overall status changed.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| oldStatus | string | None | None | The old (<a href="vim.ComputeResource.Summary.md#overallStatus">status</a>). |
| newStatus | string | None | None | The new (<a href="vim.ComputeResource.Summary.md#overallStatus">status</a>). |


