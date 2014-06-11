vim.host.PowerSystem.PowerPolicy
================================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


Power Management Policy data object.      Used to retrieve and specify current host power management policy.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | int | None | None | Power Policy Key.      Internally generated key which uniquely identifies power management    policy on a host. |
| name | string | None | None | Power Policy Name. |
| shortName | string | None | None | Power Policy Short Name.      This is not localizable property which can be used to identify specific    power managing policies like "custom" power policy.  Custom power policy    has short name set to "custom". |
| description | string | None | None | Power Policy Description. |


