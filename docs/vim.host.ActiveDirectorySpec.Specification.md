vim.host.ActiveDirectorySpec.Specification
==========================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.host.ActiveDirectorySpec.Specification.md">HostActiveDirectorySpec</a> data object defines   properties for Active Directory domain access.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| domainName | string | true | None | Domain name. |
| userName | string | true | None | Name of an Active Directory account with the authority  to add a host to the domain. |
| password | string | true | None | Password for the Active Directory account. |
| camServer | string | true | None | If set, the CAM server will be used to join the domain  and the <code>userName</code> and <code>password</code> fields  will be ignored. |
| thumbprint | string | true | None | Thumbprint for the SSL certficate of CAM server |


