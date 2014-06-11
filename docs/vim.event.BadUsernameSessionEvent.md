vim.event.BadUsernameSessionEvent
=================================
inherits from [vim.event.SessionEvent](docs/vim.event.SessionEvent.md)


This event records a failed user logon. Failed logons are due to no match existing   between the provided user name and password combination and the combinations   stored for authentication.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ipAddress | string | None | None | The IP address of the peer that initiated the connection. This may   be the client that originated the session, or it may be an intervening   proxy if the binding uses a protocol that supports proxies, such as HTTP. |


