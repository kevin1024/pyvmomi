vim.host.InternetScsiHba.DiscoveryCapabilities
==============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The discovery capabilities for this host bus adapter.   At least one discovery mode must always be active.   Multiple modes may be active at the same time.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| iSnsDiscoverySettable | bool | None | None | True if this host bus adapter supports iSNS |
| slpDiscoverySettable | bool | None | None | True if this host bus adapter supports SLP |
| staticTargetDiscoverySettable | bool | None | None | True if this host bus adapter supports static discovery |
| sendTargetsDiscoverySettable | bool | None | None | True if this host bus adapter supports changing the configuration  state of send targets discovery.  Send targets is mandatory, however  some adapters may not allow disabling this discovery method. |


