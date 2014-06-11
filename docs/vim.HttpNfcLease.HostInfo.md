vim.HttpNfcLease.HostInfo
=========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Contains information about how to connect to a given host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| url | string | None | None | The host url will be of the form  <pre>https://hostname/nfc/ticket id/</pre>  The url can be used for both POST requests to a single device and for  multi-POST requests to multiple devices. A single-POST URL is formed  by adding the target id to the hostUrl:    <pre>https://hostname/nfc/ticket id/target id</pre>  a multi-POST URL looks like    <pre>https://hostname/nfc/ticket id/multi?targets=id1,id2,id3,...</pre> |
| sslThumbprint | string | None | None | SSL thumbprint for the host the URL refers to. Empty if no SSL thumbprint  is available or needed. |


