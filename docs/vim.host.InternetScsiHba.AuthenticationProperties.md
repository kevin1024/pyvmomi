vim.host.InternetScsiHba.AuthenticationProperties
=================================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


The authentication settings for this host bus adapter or target.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| chapAuthEnabled | bool | None | None | True if CHAP is currently enabled |
| chapName | string | true | None | The CHAP user name if enabled |
| chapSecret | string | true | None | The CHAP secret if enabled |
| chapAuthenticationType | string | true | None | The preference for CHAP or non-CHAP protocol if CHAP is enabled |
| chapInherited | bool | true | None | CHAP settings are inherited |
| mutualChapName | string | true | None | When Mutual-CHAP is enabled, the user name that target needs to    use to authenticate with the initiator |
| mutualChapSecret | string | true | None | When Mutual-CHAP is enabled, the secret that target needs to    use to authenticate with the initiator |
| mutualChapAuthenticationType | string | true | None | The preference for CHAP or non-CHAP protocol if CHAP is enabled |
| mutualChapInherited | bool | true | None | Mutual-CHAP settings are inherited |


