vim.action.SendEmailAction
==========================
inherits from [vim.action.Action](docs/vim.action.Action.md)


This data object type defines an email that is triggered by an    alarm. You can use any    elements of the <a href="vim.action.Action.ActionParameter.md">ActionParameter</a>    enumerated list as part of your strings to provide information available    at runtime.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| toList | string | None | None | A comma-separated list of addresses to which the email notification is sent. |
| ccList | string | None | None | A comma-separated list of addresses that are cc'ed on the email notification. |
| subject | string | None | None | Subject of the email notification. |
| body | string | None | None | Content of the email notification. |


