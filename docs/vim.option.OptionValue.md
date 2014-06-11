vim.option.OptionValue
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Describes the key/value pair of a configured option.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | The name of the option using dot notation to reflect the    option's position in a hierarchy.  For example, you might    have an option called "Ethernet" and another option that is    a child of that called "Connection".  In this case, the key    for the latter could be defined as "Ethernet.Connection" |
| value | object | true | None | The value of the option. The Any data object type enables you to    define any value for the option. Typically, however, the value    of an option is of type String or Integer. |


