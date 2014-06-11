vim.host.InternetScsiHba.ParamValue
===================================
inherits from [vim.option.OptionValue](docs/vim.option.OptionValue.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Describes the the value of an iSCSI parameter, and whether    the value is being inherited.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| isInherited | bool | true | None | Indicates if the value is inherited from some other source.     If unset, the value is not inheritable.   isInherited can be modified only if it has already been set.      If value is to being modified, isInherited should be set to true.   Setting isInherited to false will result in the value being   once again inherited from the source. |


