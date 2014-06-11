vim.vm.QuestionInfo
===================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes the question that is currently   blocking a virtual machine.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | Identifier with an opaque value that specifies the pending question. |
| text | string | None | None | Text that describes the pending question. |
| choice | [vim.option.ChoiceOption](vim.option.ChoiceOption.md "vim.option.ChoiceOption") | None | None | List of key-value pairs that specify possible answers. |
| message | [vim.vm.Message](vim.vm.Message.md "vim.vm.Message") | true | None | The message data for the individual messages that comprise the question.  Only available on servers that support localization. |


