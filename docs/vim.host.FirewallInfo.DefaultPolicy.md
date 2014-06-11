vim.host.FirewallInfo.DefaultPolicy
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Default settings for the firewall, used for ports   that are not explicitly opened.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| incomingBlocked | bool | true | None | Flag indicating whether incoming traffic should be blocked by default. |
| outgoingBlocked | bool | true | None | Flag indicating whether outgoing traffic should be blocked by default. |


