vim.host.IscsiManager
=====================
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This managed object provides interfaces for mapping VMkernel NIC to   iSCSI Host Bus Adapter.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


QueryVnicStatus([vnicDevice](#string "string"))
-----------------------------------------------
 raises [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault")

---
| service name | QueryVnicStatus |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault") | For any problem that is not handled with a more specific fault. |




QueryPnicStatus([pnicDevice](#string "string"))
-----------------------------------------------
 raises [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault")

---
| service name | QueryPnicStatus |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault") | For any problem that is not handled with a more specific fault. |




QueryBoundVnics([iScsiHbaName](#string "string"))
-------------------------------------------------
 raises [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryBoundVnics |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault") | For any problem that is not handled with a more specific fault. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If the given HBA is not found |




QueryCandidateNics([iScsiHbaName](#string "string"))
----------------------------------------------------
 raises [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryCandidateNics |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault") | For any problem that is not handled with a more specific fault. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If the given HBA is not found |




BindVnic([iScsiHbaName](#string "string"), [vnicDevice](#string "string"))
--------------------------------------------------------------------------
 raises [vim.fault.IscsiFaultVnicHasMultipleUplinks](vim.fault.IscsiFaultVnicHasMultipleUplinks.md "vim.fault.IscsiFaultVnicHasMultipleUplinks"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.IscsiFaultVnicAlreadyBound](vim.fault.IscsiFaultVnicAlreadyBound.md "vim.fault.IscsiFaultVnicAlreadyBound"), [vim.fault.IscsiFaultVnicHasWrongUplink](vim.fault.IscsiFaultVnicHasWrongUplink.md "vim.fault.IscsiFaultVnicHasWrongUplink"), [vim.fault.IscsiFaultVnicNotFound](vim.fault.IscsiFaultVnicNotFound.md "vim.fault.IscsiFaultVnicNotFound"), [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault"), [vim.fault.IscsiFaultVnicHasNoUplinks](vim.fault.IscsiFaultVnicHasNoUplinks.md "vim.fault.IscsiFaultVnicHasNoUplinks"), [vim.fault.IscsiFaultInvalidVnic](vim.fault.IscsiFaultInvalidVnic.md "vim.fault.IscsiFaultInvalidVnic")

---
| service name | BindVnic |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IscsiFaultVnicAlreadyBound](vim.fault.IscsiFaultVnicAlreadyBound.md "vim.fault.IscsiFaultVnicAlreadyBound") | The given Virtual NIC is already bound to the HBA. |
| [vim.fault.IscsiFaultVnicHasNoUplinks](vim.fault.IscsiFaultVnicHasNoUplinks.md "vim.fault.IscsiFaultVnicHasNoUplinks") | The given Virtual NIC has no physical uplinks. |
| [vim.fault.IscsiFaultVnicHasMultipleUplinks](vim.fault.IscsiFaultVnicHasMultipleUplinks.md "vim.fault.IscsiFaultVnicHasMultipleUplinks") | The given Virtual NIC has multiple uplinks. |
| [vim.fault.IscsiFaultVnicHasWrongUplink](vim.fault.IscsiFaultVnicHasWrongUplink.md "vim.fault.IscsiFaultVnicHasWrongUplink") | The given Virtual NIC has the wrong uplink and                                        it can't be used for iSCSI multi-pathing. |
| [vim.fault.IscsiFaultVnicNotFound](vim.fault.IscsiFaultVnicNotFound.md "vim.fault.IscsiFaultVnicNotFound") | The given Virtual NIC is not present on the system. |
| [vim.fault.IscsiFaultInvalidVnic](vim.fault.IscsiFaultInvalidVnic.md "vim.fault.IscsiFaultInvalidVnic") | The given Virtual NIC is not valid for the HBA. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | For platform error that occurs during the operation. |
| [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault") | For any problem that is not handled with a more specific fault. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If the given HBA is not found |




UnbindVnic([iScsiHbaName](#string "string"), [vnicDevice](#string "string"))
----------------------------------------------------------------------------
 raises [vim.fault.IscsiFaultVnicHasActivePaths](vim.fault.IscsiFaultVnicHasActivePaths.md "vim.fault.IscsiFaultVnicHasActivePaths"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault"), [vim.fault.IscsiFaultVnicIsLastPath](vim.fault.IscsiFaultVnicIsLastPath.md "vim.fault.IscsiFaultVnicIsLastPath"), [vim.fault.IscsiFaultVnicNotBound](vim.fault.IscsiFaultVnicNotBound.md "vim.fault.IscsiFaultVnicNotBound")

---
| service name | UnbindVnic |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.IscsiFaultVnicNotBound](vim.fault.IscsiFaultVnicNotBound.md "vim.fault.IscsiFaultVnicNotBound") | The given Virtual NIC is not bound to the adapter |
| [vim.fault.IscsiFaultVnicHasActivePaths](vim.fault.IscsiFaultVnicHasActivePaths.md "vim.fault.IscsiFaultVnicHasActivePaths") | The given Virtual NIC is associated with "active" paths                                        to the storage. |
| [vim.fault.IscsiFaultVnicIsLastPath](vim.fault.IscsiFaultVnicIsLastPath.md "vim.fault.IscsiFaultVnicIsLastPath") | The given Virtual NIC is associated with "only" paths                                    to the storage. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | For platform error that occurs during the operation. |
| [vim.fault.IscsiFault](vim.fault.IscsiFault.md "vim.fault.IscsiFault") | For any problem that is not handled with a more specific fault. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If the given HBA is not found |




QueryMigrationDependencies([pnicDevice](#string "string"))
----------------------------------------------------------

| service name | QueryMigrationDependencies |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version7) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




