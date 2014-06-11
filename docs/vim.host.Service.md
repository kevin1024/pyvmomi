vim.host.Service
================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Data object that describes a single service that runs on the host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | Brief identifier for the service. |
| label | string | None | None | Display label for the service. |
| required | bool | None | None | Flag indicating whether the service is required and cannot be disabled. |
| uninstallable | bool | None | None | Flag indicating whether the service can be uninstalled. |
| running | bool | None | None | Flag indicating whether the service is currently running. |
| ruleset | string | true | None | List of firewall rulesets used by this service.  Must come from the   list of rulesets in <a href="vim.host.FirewallInfo.md#ruleset">ruleset</a>. |
| policy | string | None | None | Service activation policy.<br>See Policy |
| sourcePackage | [vim.host.Service.SourcePackage](vim.host.Service.SourcePackage.md "vim.host.Service.SourcePackage") | true | None | The source package associated with the service |


