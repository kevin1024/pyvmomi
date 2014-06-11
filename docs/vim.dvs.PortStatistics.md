vim.dvs.PortStatistics
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Statistic data of a DistributedVirtualPort.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| packetsInMulticast | long | None | None | The number of multicast packets received. |
| packetsOutMulticast | long | None | None | The number of multicast packets forwarded. |
| bytesInMulticast | long | None | None | The number of bytes received from multicast packets. |
| bytesOutMulticast | long | None | None | The number of bytes forwarded from multicast packets. |
| packetsInUnicast | long | None | None | The number of unicast packets received. |
| packetsOutUnicast | long | None | None | The number of unicast packets forwarded. |
| bytesInUnicast | long | None | None | The number of bytes received from unicast packets. |
| bytesOutUnicast | long | None | None | The number of bytes forwarded from unicast packets. |
| packetsInBroadcast | long | None | None | The number of broadcast packets received. |
| packetsOutBroadcast | long | None | None | The number of broadcast packets forwarded. |
| bytesInBroadcast | long | None | None | The number of bytes received from broadcast packets. |
| bytesOutBroadcast | long | None | None | The number of bytes forwarded from broadcast packets. |
| packetsInDropped | long | None | None | The number of received packets dropped. |
| packetsOutDropped | long | None | None | The number of packets to be forwarded dropped. |
| packetsInException | long | None | None | The number of packets received that cause an exception. |
| packetsOutException | long | None | None | The number of packets to be forwarded that cause an exception. |


