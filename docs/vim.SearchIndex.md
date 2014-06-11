vim.SearchIndex
===============


The SearchIndex service allows a client to efficiently query the   inventory for a specific managed entity by attributes such as UUID, IP address, DNS    name, or datastore path. Such searches typically return a VirtualMachine or a    HostSystem. While searching, only objects for which the user has sufficient    privileges are considered. The findByInventoryPath and findChild operations only    search on entities for which the user has view privileges; all other SearchIndex    find operations only search virtual machines and hosts for which the user has    read privileges. If the user does not have sufficient privileges for an object that    matches the search criteria, that object is not returned.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


FindByUuid([datacenter](vim.Datacenter.md "vim.Datacenter"), [uuid](#string "string"))
--------------------------------------------------------------------------------------

| service name | FindByUuid |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindByDatastorePath([datacenter](vim.Datacenter.md "vim.Datacenter"), [path](#string "string"))
-----------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore")

---
| service name | FindByDatastorePath |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidDatastore](vim.fault.InvalidDatastore.md "vim.fault.InvalidDatastore") | if a datastore has not been specified in the path or if    the specified datastore does not exist on the specified datacenter. |




FindByDnsName([datacenter](vim.Datacenter.md "vim.Datacenter"), [dnsName](#string "string"))
--------------------------------------------------------------------------------------------

| service name | FindByDnsName |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindByIp([datacenter](vim.Datacenter.md "vim.Datacenter"), [ip](#string "string"))
----------------------------------------------------------------------------------

| service name | FindByIp |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindByInventoryPath([inventoryPath](#string "string"))
------------------------------------------------------

| service name | FindByInventoryPath |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindChild([entity](vim.ManagedEntity.md "vim.ManagedEntity"), [name](#string "string"))
---------------------------------------------------------------------------------------

| service name | FindChild |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindAllByUuid([datacenter](vim.Datacenter.md "vim.Datacenter"), [uuid](#string "string"))
-----------------------------------------------------------------------------------------

| service name | FindAllByUuid |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindAllByDnsName([datacenter](vim.Datacenter.md "vim.Datacenter"), [dnsName](#string "string"))
-----------------------------------------------------------------------------------------------

| service name | FindAllByDnsName |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




FindAllByIp([datacenter](vim.Datacenter.md "vim.Datacenter"), [ip](#string "string"))
-------------------------------------------------------------------------------------

| service name | FindAllByIp |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




