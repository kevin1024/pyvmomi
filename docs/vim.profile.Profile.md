vim.profile.Profile
===================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <code>Profile</code> managed object is the base class for host and cluster  profiles.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='config'>config</a> | [vim.profile.Profile.ConfigInfo](vim.profile.Profile.ConfigInfo.md "vim.profile.Profile.ConfigInfo") | None | Profile.Edit | Configuration data for the profile. |
| <a href='description'>description</a> | [vim.profile.Profile.Description](vim.profile.Profile.Description.md "vim.profile.Profile.Description") | true | None | Localizable description of the profile |
| <a href='name'>name</a> | string | None | None | Name of the profile. |
| <a href='createdTime'>createdTime</a> | datetime | None | None | Time at which the profile was created. |
| <a href='modifiedTime'>modifiedTime</a> | datetime | None | None | Time at which the profile was last modified. |
| <a href='entity'>entity</a> | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | List of managed entities associated with the profile. |
| <a href='complianceStatus'>complianceStatus</a> | string | None | None | Overall compliance of entities associated with this profile.  If one of the entities is out of compliance, the profile is <code>nonCompliant</code>.  If all entities are in compliance, the profile is <code>compliant</code>.  If the compliance status of one of the entities is not known, compliance status   of the profile is <code>unknown</code>.  See <a href="vim.profile.ComplianceResult.Status.md">ComplianceResultStatus</a>. |


RetrieveDescription()
---------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost")

---
| service name | RetrieveDescription |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with  the profile is incompatible or there is no reference host for the profile. |




DestroyProfile()
----------------

| service name | DestroyProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Delete |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




AssociateProfile([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
--------------------------------------------------------------------
 raises [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | AssociateProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidType](vmodl.fault.InvalidType.md "vmodl.fault.InvalidType") | If the entity is of an unexpeted type. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the association conflicts with     existing association. |




DissociateProfile([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
---------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | DissociateProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the dissociation conflicts with     existing association. |




CheckProfileCompliance([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
--------------------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost")

---
| service name | CheckProfileCompliance |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with  the profile is incompatible or there is no reference host for the profile. |




ExportProfile()
---------------

| service name | ExportProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Export |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




