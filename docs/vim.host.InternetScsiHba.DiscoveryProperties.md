vim.host.InternetScsiHba.DiscoveryProperties
============================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The discovery settings for this host bus adapter.   At least one discovery mode must always be active.   Multiple modes may be active at the same time.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| iSnsDiscoveryEnabled | bool | None | None | True if iSNS is currently enabled |
| iSnsDiscoveryMethod | string | true | None | The iSNS discovery method in use when iSNS is enabled.   Must be one of the values of   <a href="vim.host.InternetScsiHba.DiscoveryProperties.ISnsDiscoveryMethod.md">InternetScsiSnsDiscoveryMethod</a> |
| iSnsHost | string | true | None | For STATIC iSNS, this is the iSNS server address |
| slpDiscoveryEnabled | bool | None | None | True if SLP is enabled |
| slpDiscoveryMethod | string | true | None | The current SLP discovery method when SLP is enabled.   Must be one of the values of   <a href="vim.host.InternetScsiHba.DiscoveryProperties.SlpDiscoveryMethod.md">SlpDiscoveryMethod</a> |
| slpHost | string | true | None | When the SLP discovery method is set to MANUAL, this property  reflects the hostname, and optionally port number of the SLP DA. |
| staticTargetDiscoveryEnabled | bool | None | None | True if static target discovery is enabled |
| sendTargetsDiscoveryEnabled | bool | None | None | True if send targets discovery is enabled |


