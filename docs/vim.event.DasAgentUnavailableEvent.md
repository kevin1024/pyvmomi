vim.event.DasAgentUnavailableEvent
==================================
inherits from [vim.event.ClusterEvent](docs/vim.event.ClusterEvent.md)
### DEPRECATED



This event records that VirtualCenter cannot contact any primary host  in this HA cluster. HA designates some hosts as primary hosts in the HA  cluster. When adding a new host to an existing cluster, HA needs to  contact one of the primary hosts to finish the configuration. VirtualCenter  has lost contact with all primary nodes in the connected state. Attempts  to configure HA on a host in this cluster will fail until a  DasAgentFoundEvent is logged or unless this is the first node to be  configured. For example, if all the other hosts are disconnected first.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


