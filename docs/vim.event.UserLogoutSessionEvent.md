vim.event.UserLogoutSessionEvent
================================
inherits from [vim.event.SessionEvent](docs/vim.event.SessionEvent.md)


This event records a user logoff, disconnection, or session timeout.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | true | None | The IP address of client |
| userAgent | string | true | None | The user agent or application |
| callCount | long | true | None | Number of API invocations made by the session |
| sessionId | string | true | None | The unique identifier for the session. |
| loginTime | datetime | true | None | Timestamp when the user logged on for this session. |


