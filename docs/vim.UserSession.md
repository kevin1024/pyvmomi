vim.UserSession
===============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


Information about a current user session.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| key | string | None | None | A unique identifier for this session,   also known as the session ID. |
| userName | string | None | None | The user name represented by this session. |
| fullName | string | None | None | The full name of the user, if available. |
| loginTime | datetime | None | None | Timestamp when the user last logged on to the server. |
| lastActiveTime | datetime | None | None | Timestamp when the user last executed a command. |
| locale | string | None | None | The locale for the session used for data formatting and preferred for messages. |
| messageLocale | string | None | None | The locale used for messages for the session.  If there are no localized messages for the user-specified locale, then  the server determines this locale. |
| extensionSession | bool | None | None | Whether or not this session belongs to a VC Extension. |
| ipAddress | string | None | None | The client identity. It could be IP address, or pipe name depended  on client binding |
| userAgent | string | None | None | The name of user agent or application |
| callCount | long | None | None | Number of API invocations since the session started |


