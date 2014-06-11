vim.host.InternetScsiHba.AuthenticationCapabilities
===================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The authentication capabilities for this host bus adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| chapAuthSettable | bool | None | None | True if this host bus adapter supports changing the configuration  state of CHAP authentication.  CHAP is mandatory, however some  adapter may not allow disabling this authentication method. |
| krb5AuthSettable | bool | None | None | Always false in this version of the API. |
| srpAuthSettable | bool | None | None | Always false in this version of the API. |
| spkmAuthSettable | bool | None | None | Always false in this version of the API. |
| mutualChapSettable | bool | true | None | When chapAuthSettable is TRUE, this describes if Mutual CHAP  configuration is allowed as well. |
| targetChapSettable | bool | true | None | When targetChapSettable is TRUE, this describes if   CHAP configuration is allowed on targets associated  with the adapter. |
| targetMutualChapSettable | bool | true | None | When targetMutualChapSettable is TRUE, this describes if   Mutual CHAP configuration is allowed on targets associated  with the adapter. |


