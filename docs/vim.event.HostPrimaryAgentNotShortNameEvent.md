vim.event.HostPrimaryAgentNotShortNameEvent
===========================================
inherits from [vim.event.HostDasEvent](docs/vim.event.HostDasEvent.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)
### DEPRECATED



This event records that the primary agent specified is not a short name.   The name of the primary agent is usually stored as a short name. You should   not normally see this error. Please check the network configurations of your   hosts.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| primaryAgent | string | None | None |  |


