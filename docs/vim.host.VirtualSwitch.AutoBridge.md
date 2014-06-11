vim.host.VirtualSwitch.AutoBridge
=================================
inherits from [vim.host.VirtualSwitch.Bridge](docs/vim.host.VirtualSwitch.Bridge.md)


This data type describes a bridge that automatically selects   a particular physical network adapter on the host   according to some predetermined policy.  Used primarily to support mobility   scenarios.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| excludedNicDevice | string | true | None | List of physical network adapters that have been excluded from   participating in the AutoBridge |


