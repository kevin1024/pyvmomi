vim.host.NatService.NameServiceSpec
===================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [VI API 2.5](vim.version.md#vim.version.version2)


This data object type specifies the information for the    name servers.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dnsAutoDetect | bool | None | None | The flag to indicate whether or not the DNS server should   be automatically detected or specified explicitly. |
| dnsPolicy | string | None | None | The policy to use when multiple DNS addresses are available    on the host. |
| dnsRetries | int | None | None | The number of retries before giving up on a DNS request    from a virtual network. |
| dnsTimeout | int | None | None | The time (in seconds) before retrying a DNS request to an external    network. |
| dnsNameServer | string | true | None | The list of DNS servers. |
| nbdsTimeout | int | None | None | The time (in seconds) allotted for queries to the NetBIOS    Datagram Server (NBDS). |
| nbnsRetries | int | None | None | Number of retries for each query to the NBNS. |
| nbnsTimeout | int | None | None | The time (in seconds) allotted for queries to the NBNS. |


