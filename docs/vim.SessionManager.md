vim.SessionManager
==================


This managed object type includes methods for logging on and   logging off clients, determining which clients are currently   logged on, and forcing clients to log off.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='sessionList'>sessionList</a> | [vim.UserSession](vim.UserSession.md "vim.UserSession") | true | Sessions.TerminateSession | The list of currently active sessions. |
| <a href='currentSession'>currentSession</a> | [vim.UserSession](vim.UserSession.md "vim.UserSession") | true | System.Anonymous | This property contains information about the client's current session.   If the client is not logged on, the value is null. |
| <a href='message'>message</a> | string | true | System.View | The system global message from the server. |
| <a href='messageLocaleList'>messageLocaleList</a> | string | true | System.Anonymous | Provides the list of locales for which the server has localized messages. |
| <a href='supportedLocaleList'>supportedLocaleList</a> | string | true | System.Anonymous | Provides the list of locales that the server supports.   Listing a locale ensures that some standardized information such as dates appear   in the appropriate format. Other localized information, such as error messages,   are displayed, if available. If localized information is not available, the   message is returned using the system locale. |
| <a href='defaultLocale'>defaultLocale</a> | string | None | System.Anonymous | This is the default server locale. |


UpdateServiceMessage([message](#string "string"))
-------------------------------------------------

| service name | UpdateServiceMessage |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Sessions.GlobalMessage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




LoginByToken([locale](#string "string"))
----------------------------------------
 raises [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission")

---
| service name | LoginByToken |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if there is no token provided or the token                        could not be validated. |
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | if the locale is invalid or unknown to the server. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if the principal is valid, but has no access granted. |




Login([userName](#string "string"), [password](#string "string"), [locale](#string "string"))
---------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission")

---
| service name | Login |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the user and password combination is invalid. |
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | if the locale is invalid or unknown to the server. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if the user is valid, but has no access granted. |




LoginBySSPI([base64Token](#string "string"), [locale](#string "string"))
------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale"), [vim.fault.SSPIChallenge](vim.fault.SSPIChallenge.md "vim.fault.SSPIChallenge"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission")

---
| service name | LoginBySSPI |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.SSPIChallenge](vim.fault.SSPIChallenge.md "vim.fault.SSPIChallenge") | if further negotiation is required. |
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the user context could not be passed successfully,                        or the context is not valid on the server. |
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | if the locale is invalid or unknown to the server. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if the user is valid, but has no access granted. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the service does not support SSPI authentication. |




Logout()
--------

| service name | Logout |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AcquireLocalTicket([userName](#string "string"))
------------------------------------------------
 raises [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | AcquireLocalTicket |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the userName is invalid. |
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if the user and password are valid, but the user has no access          granted. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the server does not support this operation. |




AcquireGenericServiceTicket([spec](vim.SessionManager.ServiceRequestSpec.md "vim.SessionManager.ServiceRequestSpec"))
---------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission"), [vim.fault.NotAuthenticated](vim.fault.NotAuthenticated.md "vim.fault.NotAuthenticated")

---
| service name | AcquireGenericServiceTicket |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NoPermission](vim.fault.NoPermission.md "vim.fault.NoPermission") | if the client does not have enough privileges to                        be granted a ticket. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the spec is not supported or not valid. |
| [vim.fault.NotAuthenticated](vim.fault.NotAuthenticated.md "vim.fault.NotAuthenticated") | if the current session is not authenticated                            for clone session request |




TerminateSession([sessionId](#string "string"))
-----------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | TerminateSession |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Sessions.TerminateSession |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a sessionId could not be found as a valid logged-on session. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if a sessionId matches the current session.  Use                            the logout method to terminate the current session. |




SetLocale([locale](#string "string"))
-------------------------------------
 raises [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale")

---
| service name | SetLocale |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | if the locale is invalid or unknown to the server. |




LoginExtensionBySubjectName([extensionKey](#string "string"), [locale](#string "string"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.NoClientCertificate](vim.fault.NoClientCertificate.md "vim.fault.NoClientCertificate"), [vim.fault.InvalidClientCertificate](vim.fault.InvalidClientCertificate.md "vim.fault.InvalidClientCertificate"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale"), [vim.fault.NoSubjectName](vim.fault.NoSubjectName.md "vim.fault.NoSubjectName")

---
| service name | LoginExtensionBySubjectName |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the extension is not registered, or the subject name                        doesn't match the subject name of the extension. |
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | if the supplied locale is not valid |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if no extension is associated with the given key |
| [vim.fault.NoClientCertificate](vim.fault.NoClientCertificate.md "vim.fault.NoClientCertificate") | if no certificate was used by the client to connect |
| [vim.fault.NoSubjectName](vim.fault.NoSubjectName.md "vim.fault.NoSubjectName") | if the extension was registered without a subject name |
| [vim.fault.InvalidClientCertificate](vim.fault.InvalidClientCertificate.md "vim.fault.InvalidClientCertificate") | if the client cerificate fails the verification at the server |




LoginExtensionByCertificate([extensionKey](#string "string"), [locale](#string "string"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.NoClientCertificate](vim.fault.NoClientCertificate.md "vim.fault.NoClientCertificate"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale")

---
| service name | LoginExtensionByCertificate |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the extension is not registered, or the                        certificate does not match the expected value. |
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | if the supplied locale is not valid |
| [vim.fault.NoClientCertificate](vim.fault.NoClientCertificate.md "vim.fault.NoClientCertificate") | if no certificate was used by the client to connect |




ImpersonateUser([userName](#string "string"), [locale](#string "string"))
-------------------------------------------------------------------------
 raises [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale")

---
| service name | ImpersonateUser |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Sessions.ImpersonateUser |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | vim.fault.InvalidLogin |
| [vim.fault.InvalidLocale](vim.fault.InvalidLocale.md "vim.fault.InvalidLocale") | vim.fault.InvalidLocale |




SessionIsActive([sessionID](#string "string"), [userName](#string "string"))
----------------------------------------------------------------------------

| service name | SessionIsActive |
|:--|:--|
| since version | [VI API 2.5](vim.version.md#None) |
| privilege    | Sessions.ValidateSession |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|




AcquireCloneTicket()
--------------------
 raises [vim.fault.NotAuthenticated](vim.fault.NotAuthenticated.md "vim.fault.NotAuthenticated")

---
| service name | AcquireCloneTicket |
|:--|:--|
| since version | [VI API 2.5u2](vim.version.md#None) |
| privilege    | System.View |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotAuthenticated](vim.fault.NotAuthenticated.md "vim.fault.NotAuthenticated") | if the current session is not authenticated<br>See <a href="vim.SessionManager.md#cloneSession">CloneSession</a><br> |




CloneSession([cloneTicket](#string "string"))
---------------------------------------------
 raises [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | CloneSession |
|:--|:--|
| since version | [VI API 2.5u2](vim.version.md#None) |
| privilege    | System.Anonymous |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if the specified ticket value is not valid.<br>See <a href="vim.SessionManager.md#acquireCloneTicket">AcquireCloneTicket</a><br>See <a href="vim.SessionManager.md#acquireGenericServiceTicket">AcquireGenericServiceTicket</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the server does not support this operation.<br>See <a href="vim.SessionManager.md#acquireCloneTicket">AcquireCloneTicket</a><br>See <a href="vim.SessionManager.md#acquireGenericServiceTicket">AcquireGenericServiceTicket</a><br> |




