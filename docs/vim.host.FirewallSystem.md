vim.host.FirewallSystem
=======================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


The FirewallSystem managed object describes the firewall configuration   of the host.   <p>   The firewall should be configured first by setting the default policy and   then by making exceptions to the policy to get the desired openness.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='firewallInfo'>firewallInfo</a> | [vim.host.FirewallInfo](vim.host.FirewallInfo.md "vim.host.FirewallInfo") | true | None | Firewall configuration. |


UpdateDefaultPolicy([defaultPolicy](vim.host.FirewallInfo.DefaultPolicy.md "vim.host.FirewallInfo.DefaultPolicy"))
------------------------------------------------------------------------------------------------------------------

| service name | UpdateDefaultPolicy |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




EnableRuleset([id](#string "string"))
-------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | EnableRuleset |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the ruleset ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if an internal error happend when reconfigure the                           ruleset. |




DisableRuleset([id](#string "string"))
--------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DisableRuleset |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the ruleset ID is unknown. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if an internal error happend when reconfigure the                           ruleset. |




UpdateRuleset([id](#string "string"), [spec](vim.host.Ruleset.RulesetSpec.md "vim.host.Ruleset.RulesetSpec"))
-------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateRuleset |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the ruleset ID is unknown |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the update of the ruleset failed. |




RefreshFirewall()
-----------------

| service name | RefreshFirewall |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.NetService |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




