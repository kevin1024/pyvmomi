vim.vm.guest.NamePasswordAuthentication
=======================================
inherits from [vim.vm.guest.GuestAuthentication](docs/vim.vm.guest.GuestAuthentication.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


NamePasswordAuthentication contains the information necessary to authenticate   within a guest using a name and password. This is the typical method for   authentication within a guest and the one currently used by VIX.   This method of authentication is stateless.   <p>   To use NamePasswordAuthentication, populate username and password with the   appropriate login information. You should not use <a href="vim.vm.guest.AuthManager.md#acquireCredentials">AcquireCredentialsInGuest</a>   or <a href="vim.vm.guest.AuthManager.md#releaseCredentials">ReleaseCredentialsInGuest</a> for NamePasswordAuthentication.   <p>   Once populated, you can use NamePasswordAuthentication in any guest operations function call.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| username | string | None | None | The user name for Name-Password authentication. |
| password | string | None | None | The password for Name-Password authentication. |


