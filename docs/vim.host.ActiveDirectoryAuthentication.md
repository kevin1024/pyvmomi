vim.host.ActiveDirectoryAuthentication
======================================
inherits from [vim.host.DirectoryStore](vim.host.DirectoryStore.md "vim.host.DirectoryStore")
as of [vSphere API 4.1](vim.version.md#vim.version.version6)


The <a href="vim.host.ActiveDirectoryAuthentication.md">HostActiveDirectoryAuthentication</a> managed object   indicates domain membership status and provides methods   for adding a host to and removing a host from a domain.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


JoinDomain([domainName](#string "string"), [userName](#string "string"), [password](#string "string"))
------------------------------------------------------------------------------------------------------
 raises [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidHostName](vim.fault.InvalidHostName.md "vim.fault.InvalidHostName"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.DomainNotFound](vim.fault.DomainNotFound.md "vim.fault.DomainNotFound"), [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin"), [vim.fault.ClockSkew](vim.fault.ClockSkew.md "vim.fault.ClockSkew"), [vim.fault.NoPermissionOnAD](vim.fault.NoPermissionOnAD.md "vim.fault.NoPermissionOnAD"), [vim.fault.BlockedByFirewall](vim.fault.BlockedByFirewall.md "vim.fault.BlockedByFirewall")

---
| service name | JoinDomain |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version6) |
| privilege    | Host.Config.AuthenticationStore |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host has already joined a domain. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the host configuration prevents the join operation                           from succeeding. |
| [vim.fault.InvalidLogin](vim.fault.InvalidLogin.md "vim.fault.InvalidLogin") | if <code>userName</code> and <code>password</code>                        are not valid user credentials. |
| [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault") | for any problem that is not handled with a more specific fault. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the <a href="vim.host.ActiveDirectoryAuthentication.md">HostActiveDirectoryAuthentication</a> object is busy. |
| [vim.fault.BlockedByFirewall](vim.fault.BlockedByFirewall.md "vim.fault.BlockedByFirewall") | if ports needed by the join operation are                             blocked by the firewall. |
| [vim.fault.DomainNotFound](vim.fault.DomainNotFound.md "vim.fault.DomainNotFound") | if the domain controller for <code>domainName</code>                          cannot be reached. |
| [vim.fault.NoPermissionOnAD](vim.fault.NoPermissionOnAD.md "vim.fault.NoPermissionOnAD") | if <code>userName</code> has no right to add hosts to the domain. |
| [vim.fault.InvalidHostName](vim.fault.InvalidHostName.md "vim.fault.InvalidHostName") | if the domain part of the host's FQDN doesn't match                           the domain being joined. |
| [vim.fault.ClockSkew](vim.fault.ClockSkew.md "vim.fault.ClockSkew") | if the clocks of the host and the domain controller                     differ by more than the allowed amount of time. |




JoinDomainWithCAM([domainName](#string "string"), [camServer](#string "string"))
--------------------------------------------------------------------------------
 raises [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidCAMCertificate](vim.fault.InvalidCAMCertificate.md "vim.fault.InvalidCAMCertificate"), [vim.fault.InvalidHostName](vim.fault.InvalidHostName.md "vim.fault.InvalidHostName"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.DomainNotFound](vim.fault.DomainNotFound.md "vim.fault.DomainNotFound"), [vim.fault.ClockSkew](vim.fault.ClockSkew.md "vim.fault.ClockSkew"), [vim.fault.CAMServerRefusedConnection](vim.fault.CAMServerRefusedConnection.md "vim.fault.CAMServerRefusedConnection"), [vim.fault.InvalidCAMServer](vim.fault.InvalidCAMServer.md "vim.fault.InvalidCAMServer"), [vim.fault.BlockedByFirewall](vim.fault.BlockedByFirewall.md "vim.fault.BlockedByFirewall")

---
| service name | JoinDomainWithCAM |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | Host.Config.AuthenticationStore |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host has already joined a domain. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if the host configuration prevents the join operation                           from succeeding. |
| [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault") | for any problem that is not handled with a more specific fault. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the <a href="vim.host.ActiveDirectoryAuthentication.md">HostActiveDirectoryAuthentication</a> object is busy. |
| [vim.fault.BlockedByFirewall](vim.fault.BlockedByFirewall.md "vim.fault.BlockedByFirewall") | if ports needed by the join operation are                             blocked by the firewall. |
| [vim.fault.DomainNotFound](vim.fault.DomainNotFound.md "vim.fault.DomainNotFound") | if the domain controller for <code>domainName</code>                          cannot be reached. |
| [vim.fault.InvalidHostName](vim.fault.InvalidHostName.md "vim.fault.InvalidHostName") | if the domain part of the host's FQDN doesn't match                           the domain being joined. |
| [vim.fault.ClockSkew](vim.fault.ClockSkew.md "vim.fault.ClockSkew") | if the clocks of the host and the domain controller                     differ by more than the allowed amount of time. |
| [vim.fault.InvalidCAMServer](vim.fault.InvalidCAMServer.md "vim.fault.InvalidCAMServer") | if camServer is not a valid IP address, or                            if camServer is not accessible. |
| [vim.fault.InvalidCAMCertificate](vim.fault.InvalidCAMCertificate.md "vim.fault.InvalidCAMCertificate") | if the certificate of the given CAM server                                 cannot be verified. |
| [vim.fault.CAMServerRefusedConnection](vim.fault.CAMServerRefusedConnection.md "vim.fault.CAMServerRefusedConnection") | if the specified CAM server is not                                      reachable, or                                      if the server denied access. |




ImportCertificateForCAM([certPath](#string "string"), [camServer](#string "string"))
------------------------------------------------------------------------------------
 raises [vim.fault.InvalidCAMServer](vim.fault.InvalidCAMServer.md "vim.fault.InvalidCAMServer"), [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault"), [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound")

---
| service name | ImportCertificateForCAM |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version6) |
| privilege    | Host.Config.AuthenticationStore |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.FileNotFound](vim.fault.FileNotFound.md "vim.fault.FileNotFound") | if the certificate file does not exist |
| [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault") | for any problem that is not handled with a more specific fault. |
| [vim.fault.InvalidCAMServer](vim.fault.InvalidCAMServer.md "vim.fault.InvalidCAMServer") | if camServer is not a valid IP address |




LeaveCurrentDomain()
--------------------
 raises [vim.fault.NonADUserRequired](vim.fault.NonADUserRequired.md "vim.fault.NonADUserRequired"), [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission"), [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | LeaveCurrentDomain |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version6) |
| privilege    | Host.Config.AuthenticationStore |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in a domain or there are active                        permissions for Active Directory users. |
| [vim.fault.AuthMinimumAdminPermission](vim.fault.AuthMinimumAdminPermission.md "vim.fault.AuthMinimumAdminPermission") | if this change would leave the system with                        no Administrator permission on the root node. |
| [vim.fault.ActiveDirectoryFault](vim.fault.ActiveDirectoryFault.md "vim.fault.ActiveDirectoryFault") | for any problem that is not handled with a specific fault. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if the ActiveDirectoryAuthentication object is busy. |
| [vim.fault.NonADUserRequired](vim.fault.NonADUserRequired.md "vim.fault.NonADUserRequired") | only non Active Directory users can initiate                        the leave domain operation. |




