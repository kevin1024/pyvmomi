vim.vm.customization.Password
=============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Contains a password string and a flag that specifies whether the string is in plain   text or encrypted.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| value | string | None | None | The password string. It is encrypted if the associated plainText flag is false. |
| plainText | bool | None | None | Flag to specify whether or not the password is in plain text, rather than   encrypted. |


