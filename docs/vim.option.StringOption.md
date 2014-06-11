vim.option.StringOption
=======================
inherits from [vim.option.OptionType](docs/vim.option.OptionType.md)


The StringOption data object type is used to define an open-ended    string value based on an optional subset of valid characters.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| defaultValue | string | None | None | The default value. |
| validCharacters | string | true | None | The string containing the set of valid characters. If a string    option is not specified, all strings are allowed. |


