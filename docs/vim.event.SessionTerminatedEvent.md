vim.event.SessionTerminatedEvent
================================
inherits from [vim.event.SessionEvent](docs/vim.event.SessionEvent.md)


This event records the termination of a session.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| sessionId | string | None | None | The unique identifier of the terminated session. |
| terminatedUsername | string | None | None | The name of the user owning the terminated session. |


