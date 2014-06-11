vim.option.OptionDef
====================
inherits from [vim.ElementDescription](docs/vim.ElementDescription.md)


Describes a user-defined option. The name of each option is identified by the   "key" property, inherited from the <a href="vim.ElementDescription.md">ElementDescription</a>    data object type.   You can indicate the property's position in a hierarchy by using a dot-separated   notation. The string preceding the first dot is the top of the hierarchy. The    hierarchy descends to a new sublevel with each dot.     For example,  "Ethernet.NetworkConnection.Bridged".

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| optionType | [vim.option.OptionType](vim.option.OptionType.md "vim.option.OptionType") | None | None | The option type which defines allowed values. |


