vim.host.LinkDiscoveryProtocolConfig
====================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Dataobject representing the link discovery protocol configuration for a   virtual or distributed virtual switch.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| protocol | string | None | None | The discovery protocol type. For valid values   see <a href="vim.host.LinkDiscoveryProtocolConfig.ProtocolType.md">LinkDiscoveryProtocolConfigProtocolType</a>. |
| operation | string | None | None | Whether to advertise or listen. For valid values see   <a href="vim.host.LinkDiscoveryProtocolConfig.OperationType.md">LinkDiscoveryProtocolConfigOperationType</a>. |


