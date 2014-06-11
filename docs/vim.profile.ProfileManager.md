vim.profile.ProfileManager
==========================
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


This Class is responsible for managing Profiles.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='profile'>profile</a> | [vim.profile.Profile](vim.profile.Profile.md "vim.profile.Profile") | true | Profile.View | A list of profiles known to this ProfileManager. |


CreateProfile([createSpec](vim.profile.Profile.CreateSpec.md "vim.profile.Profile.CreateSpec"))
-----------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost"), [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | CreateProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Create |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | If a profile with the specified name already  exists. |
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the specified reference host is  incompatible or no reference host has been specifed. |




QueryPolicyMetadata([policyName](#string "string"), [profile](vim.profile.Profile.md "vim.profile.Profile"))
------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryPolicyMetadata |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If policyName is invalid. |
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with the  profile is incompatible or there is no reference host for the profile. |




FindAssociatedProfile([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
-------------------------------------------------------------------------

| service name | FindAssociatedProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




