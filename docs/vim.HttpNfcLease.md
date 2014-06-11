vim.HttpNfcLease
================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Represents a lease on a <a href="vim.VirtualMachine.md">VirtualMachine</a> or   a <a href="vim.VirtualApp.md">VirtualApp</a>, which can be used to import or export   disks for the entity. While the lease is held, operations   that alter the state of the virtual machines covered by the lease   are blocked. Examples of blocked operations are PowerOn, Destroy,   Migrate, etc.   <p>   A lease is in one of four states:    <dl>     <dt>Initializing</dt>     <dd>This is the initial state. The lease remains in this state         while the corresponding import/export task is preparing the         objects. In an import session, this involves creating         inventory objects.</dd>     <dt>Ready</dt>     <dd>The lease changes to this state once the corresponding         import/export task is done preparing the lease. The leased         objects are now ready, and the client can use the information         provided in the <a href="vim.HttpNfcLease.md#info">info</a> property to determine where to         up/download disks. The client must call <a href="vim.HttpNfcLease.md#progress">HttpNfcLeaseProgress</a>         periodically to keep the lease alive and report progress to         the corresponding import/export task. Failure to do so causes         the lease to time out and enter the error state.</dd>     <dt>Done</dt>     <dd>When the client is done transferring disks, it calls         <a href="vim.HttpNfcLease.md#complete">HttpNfcLeaseComplete</a> to signal the end of the import/export session.         This causes the corresponding import/export task to complete         successfully.</dd>     <dt>Error</dt>     <dd>If an error occurs during initialization or the lease times out,         it will change to this state. The client can also abort the lease         manually by calling <a href="vim.HttpNfcLease.md#abort">HttpNfcLeaseAbort</a>. In this state, the <a href="vim.HttpNfcLease.md#error">error</a>         property can be read to determine the cause.         If the lease belongs to an import session, all objects created         during the import are removed when the lease enters this state.</dd>   </dl>    The import/export task corresponding to the lease continues running while   the lease is held.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='initializeProgress'>initializeProgress</a> | int | None | None | Provides progress information (0-100 percent) for the initializing state   of the lease. Clients can use this to track overall progress. |
| <a href='info'>info</a> | [vim.HttpNfcLease.Info](vim.HttpNfcLease.Info.md "vim.HttpNfcLease.Info") | true | None | Provides information on the objects contained in this lease. The   info property is only valid when the lease is in the ready state. |
| <a href='state'>state</a> | [vim.HttpNfcLease.State](vim.HttpNfcLease.State.md "vim.HttpNfcLease.State") | None | None | The current state of the lease. |
| <a href='error'>error</a> | [vmodl.LocalizedMethodFault](vmodl.LocalizedMethodFault.md "vmodl.LocalizedMethodFault") | true | None | If the lease is in the error state, this property contains the   error that caused the lease to be aborted. |


HttpNfcLeaseGetManifest()
-------------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | HttpNfcLeaseGetManifest |
|:--|:--|
| since version | [vSphere API 4.1](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | vim.fault.Timedout |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | vim.fault.InvalidState |




HttpNfcLeaseComplete()
----------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | HttpNfcLeaseComplete |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | if the lease has timed out before this call. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the lease has already been completed or           aborted. |




HttpNfcLeaseAbort([fault](vmodl.MethodFault.md "vmodl.MethodFault"))
--------------------------------------------------------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | HttpNfcLeaseAbort |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | if the lease has timed out before this call. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the lease has already been aborted. |




HttpNfcLeaseProgress()
----------------------
 raises [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout")

---
| service name | HttpNfcLeaseProgress |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.Timedout](vim.fault.Timedout.md "vim.fault.Timedout") | if the lease has timed out. |




