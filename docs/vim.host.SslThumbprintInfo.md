vim.host.SslThumbprintInfo
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The SSL thumbprint information for a host managed by a vCenter Server   or a vCenter extension to login into other hosts without   username/password authentication.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| principal | string | None | None | The principal used for the login session |
| ownerTag | string | None | None | The tag associated with this registration.  Owner tags allow   multiple entities to register the same thumbprint without   interfering with each other on the life cycle of the thumbprint with   their unique tags.    Each solution should use a unique tag to identify itself. |
| sslThumbprints | string | true | None | Specify the SSL thumbprints to register on the host. |


