vim.UserDirectory
=================


The <a href="vim.UserDirectory.md">UserDirectory</a> managed object provides information about users   and groups on a vSphere server and ESX hosts. The method    <a href="vim.UserDirectory.md#retrieveUserGroups">RetrieveUserGroups</a> returns a list   of user account data. The method can perform a search operation based on   specific criteria - user name, group name, sub-string or string matching,    and, on Windows, domain. Use the results as input   to the AuthorizationManager methods    <a href="vim.AuthorizationManager.md#setEntityPermissions">SetEntityPermissions</a> and    <a href="vim.AuthorizationManager.md#resetEntityPermissions">ResetEntityPermissions</a>.   <p>   The content of the returned results depends on the server environment:   <ul>      <li> On a Windows host, <a href="vim.UserDirectory.md#retrieveUserGroups">RetrieveUserGroups</a> can search            from the set of trusted domains on the host, including the primary           domain of the system. A special domain (specified as an            empty string - &quot;&quot;) refers to the users and groups local           to the host.      <li> On an ESX Server or a Linux host, the search operates on the           users and groups defined in the /etc/passwd file. Always specify           an empty string (&quot;&quot;) for the domain argument.           If the /etc/passwd file contains Sun NIS or NIS+ users and groups,           RetrieveUserGroups returns information about these accounts as well.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='domainList'>domainList</a> | string | true | System.View | List of Windows domains available for user searches, if the underlying   system supports windows domain membership. |


RetrieveUserGroups([domain](#string "string"), [searchStr](#string "string"), [belongsToGroup](#string "string"), [belongsToUser](#string "string"))
----------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RetrieveUserGroups |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If any of the domain, belongsToGroup, or belongsToUser                        arguments refer to entities that do not exist. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | If you specify a domain for systems that do not support                        domains, such as an ESX Server. The method also throws                        NotSupported if you specify membership (belongsToGroup or                        belongsToUser) and the server does not support                        by-membership queries. |




