vim.host.FibreChannelOverEthernetHba
====================================
inherits from [vim.host.FibreChannelHba](docs/vim.host.FibreChannelHba.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This data object type describes the FCoE host bus adapter   interface.    Terminology is borrowed from T11's working draft of the Fibre Channel   Backbone 5 standard (FC-BB-5).  The draft can be found at   http://www.t11.org.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| underlyingNic | string | None | None | The name associated with this FCoE HBA's underlying FcoeNic. |
| linkInfo | [vim.host.FibreChannelOverEthernetHba.LinkInfo](vim.host.FibreChannelOverEthernetHba.LinkInfo.md "vim.host.FibreChannelOverEthernetHba.LinkInfo") | None | None | Link information that can be used to uniquely identify this FCoE HBA. |
| isSoftwareFcoe | bool | None | None | True if this host bus adapter is a software based FCoE initiator. |
| markedForRemoval | bool | None | None | True if this host bus adapter has been marked for removal. |


