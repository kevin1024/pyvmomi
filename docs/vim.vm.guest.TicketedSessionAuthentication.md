vim.vm.guest.TicketedSessionAuthentication
==========================================
inherits from [vim.vm.guest.GuestAuthentication](docs/vim.vm.guest.GuestAuthentication.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


TicketedSessionAuthentication contains the information necessary to   use previously obtained credentials in the guest.   The ticketed session is not stateless and stores state inside of the guest.   <p>   A TicketedSessionAuthentication object will be returned as the result of a   successful call to <a href="vim.vm.guest.AuthManager.md#acquireCredentials">AcquireCredentialsInGuest</a>. You can   use this object in any guest operations function call.   <p>   When you no longer need the TicketedSessionAuthentication object, you should   call <a href="vim.vm.guest.AuthManager.md#releaseCredentials">ReleaseCredentialsInGuest</a> to free associated resources   and session data.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| ticket | string | None | None | This contains a base64 encoded Ticket. |


