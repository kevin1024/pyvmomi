vim.IpPoolManager
=================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


Singleton Managed Object used to manage IP Pools.  <p>  IP Pools are used to allocate IPv4 and IPv6 addresses to vApps.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryIpPools([dc](vim.Datacenter.md "vim.Datacenter"))
------------------------------------------------------

| service name | QueryIpPools |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateIpPool([dc](vim.Datacenter.md "vim.Datacenter"), [pool](vim.vApp.IpPool.md "vim.vApp.IpPool"))
----------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CreateIpPool |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type | None |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the name of the pool already exists on the datacenter. |




UpdateIpPool([dc](vim.Datacenter.md "vim.Datacenter"), [pool](vim.vApp.IpPool.md "vim.vApp.IpPool"))
----------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdateIpPool |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the name of the pool already exists on the datacenter. |




DestroyIpPool([dc](vim.Datacenter.md "vim.Datacenter"))
-------------------------------------------------------
 raises [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | DestroyIpPool |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the pool is in use and the force flag is false |




AllocateIpv4Address([dc](vim.Datacenter.md "vim.Datacenter"), [allocationId](#string "string"))
-----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | AllocateIpv4Address |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specified IP pool does not exist on the specified datacenter. |




AllocateIpv6Address([dc](vim.Datacenter.md "vim.Datacenter"), [allocationId](#string "string"))
-----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | AllocateIpv6Address |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specified IP pool does not exist on the specified datacenter. |




ReleaseIpAllocation([dc](vim.Datacenter.md "vim.Datacenter"), [allocationId](#string "string"))
-----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | ReleaseIpAllocation |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specified IP pool does not exist on the specified datacenter. |




QueryIPAllocations([dc](vim.Datacenter.md "vim.Datacenter"), [extensionKey](#string "string"))
----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryIPAllocations |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the specified IP pool does not exist on the specified datacenter. |




