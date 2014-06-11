vim.event.UserLoginSessionEvent
===============================
inherits from [vim.event.SessionEvent](docs/vim.event.SessionEvent.md)


This event records a user logon.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | None | None | The IP address of the peer that initiated the connection. This may   be the client that originated the session, or it may be an intervening   proxy if the binding uses a protocol that supports proxies, such as HTTP. |
| userAgent | string | true | None | The user agent or application |
| locale | string | None | None | The locale of the session. |
| sessionId | string | None | None | The unique identifier for the session. |


