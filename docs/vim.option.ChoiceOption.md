vim.option.ChoiceOption
=======================
inherits from [vim.option.OptionType](docs/vim.option.OptionType.md)


The ChoiceOption data object type defines a set of   supported string values, a localizable description for each value,   and the default value.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| choiceInfo | [vim.ElementDescription](vim.ElementDescription.md "vim.ElementDescription") | None | None | The set of possible selections and descriptions. |
| defaultIndex | int | true | None | The index in ChoiceOption.value that serves as the default value. |


