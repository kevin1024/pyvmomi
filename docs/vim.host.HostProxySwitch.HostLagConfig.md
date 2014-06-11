vim.host.HostProxySwitch.HostLagConfig
======================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


This data object type describes the set of Uplink Ports in   Link Aggregation Control Protocol group.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| lagKey | string | None | None |  |
| lagName | string | true | None |  |
| uplinkPort | [vim.KeyValue](vim.KeyValue.md "vim.KeyValue") | true | None | The list of Uplink Ports in the Link Aggregation Control Protocol group.   This property contains the keys and names of such ports. |


