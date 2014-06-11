vim.host.Ruleset
================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Data object that describes a single network ruleset that can be   allowed or blocked by the firewall using the <a href="vim.host.FirewallSystem.md">HostFirewallSystem</a> object.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Brief identifier for the ruleset. |
| label | string | None | None | Display label for the ruleset. |
| required | bool | None | None | Flag indicating whether the ruleset is required and cannot be disabled. |
| rule | [vim.host.Ruleset.Rule](vim.host.Ruleset.Rule.md "vim.host.Ruleset.Rule") | None | None | List of rules within the ruleset. |
| service | string | true | None | Managed service (if any) that uses this ruleset. Must be one of   the services listed in <a href="vim.host.ServiceInfo.md#service">service</a>. |
| enabled | bool | None | None | Flag indicating whether the ruleset is enabled.  If the   ruleset is enabled, all ports specified in the ruleset are   opened by the firewall. |
| allowedHosts | [vim.host.Ruleset.IpList](vim.host.Ruleset.IpList.md "vim.host.Ruleset.IpList") | true | None | List of ipaddress to allow access to the service |


