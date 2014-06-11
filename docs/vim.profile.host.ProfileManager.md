vim.profile.host.ProfileManager
===============================
inherits from [vim.profile.ProfileManager](vim.profile.ProfileManager.md "vim.profile.ProfileManager")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.ProfileManager.md">HostProfileManager</a> provides access to a list of  <a href="vim.profile.host.HostProfile.md">HostProfile</a>s and it defines methods to manipulate  profiles and <a href="vim.profile.host.AnswerFile.md">AnswerFile</a>s.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


ApplyHostConfig([host](vim.HostSystem.md "vim.HostSystem"), [configSpec](vim.host.ConfigSpec.md "vim.host.ConfigSpec"), [userInput](vim.profile.DeferredPolicyOptionParameter.md "vim.profile.DeferredPolicyOptionParameter"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFailed](vim.fault.HostConfigFailed.md "vim.fault.HostConfigFailed"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState")

---
| service name | ApplyHostConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | dynamic |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in maintenance mode and the          configuration specification requires it. |
| [vim.fault.HostConfigFailed](vim.fault.HostConfigFailed.md "vim.fault.HostConfigFailed") | if the ESX Server cannot apply the configuration changes. |




GenerateConfigTaskList([configSpec](vim.host.ConfigSpec.md "vim.host.ConfigSpec"), [host](vim.HostSystem.md "vim.HostSystem"))
------------------------------------------------------------------------------------------------------------------------------

### Deprecated
As of vSphere API 5.5 use     <a href="vim.profile.host.ProfileManager.md#generateTaskList">GenerateHostProfileTaskList_Task</a>

| service name | GenerateConfigTaskList |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




GenerateHostProfileTaskList([configSpec](vim.host.ConfigSpec.md "vim.host.ConfigSpec"), [host](vim.HostSystem.md "vim.HostSystem"))
-----------------------------------------------------------------------------------------------------------------------------------

| service name | GenerateHostProfileTaskList |
|:--|:--|
| since version | [vSphere API 5.5](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




QueryHostProfileMetadata([profileName](#string "string"), [profile](vim.profile.Profile.md "vim.profile.Profile"))
------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | QueryHostProfileMetadata |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If profileName parameter is invalid. |
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with  the profile is incompatible or there is no reference host for the profile. |




QueryProfileStructure([profile](vim.profile.Profile.md "vim.profile.Profile"))
------------------------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost")

---
| service name | QueryProfileStructure |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with  the profile is incompatible or there is no reference host for the profile. |




CreateDefaultProfile([profileType](#string "string"), [profileTypeName](#string "string"), [profile](vim.profile.Profile.md "vim.profile.Profile"))
---------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | CreateDefaultProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If either the profileType or profileTypeName is incorrect. |
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with the profile   is incompatible or there is no reference host for the profile. |




UpdateAnswerFile([host](vim.HostSystem.md "vim.HostSystem"), [configSpec](vim.profile.host.ProfileManager.AnswerFileCreateSpec.md "vim.profile.host.ProfileManager.AnswerFileCreateSpec"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.AnswerFileUpdateFailed](vim.fault.AnswerFileUpdateFailed.md "vim.fault.AnswerFileUpdateFailed"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument")

---
| service name | UpdateAnswerFile |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Edit |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AnswerFileUpdateFailed](vim.fault.AnswerFileUpdateFailed.md "vim.fault.AnswerFileUpdateFailed") | If the answer file could not be updated. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | If the input parameteres are incorrect. |




RetrieveAnswerFile([host](vim.HostSystem.md "vim.HostSystem"))
--------------------------------------------------------------

| service name | RetrieveAnswerFile |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




RetrieveAnswerFileForProfile([host](vim.HostSystem.md "vim.HostSystem"), [applyProfile](vim.profile.host.HostApplyProfile.md "vim.profile.host.HostApplyProfile"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------

| service name | RetrieveAnswerFileForProfile |
|:--|:--|
| since version | [vSphere API 5.1](vim.version.md#vim.version.version5) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




ExportAnswerFile([host](vim.HostSystem.md "vim.HostSystem"))
------------------------------------------------------------

| service name | ExportAnswerFile |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Export |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|




CheckAnswerFileStatus([host](vim.HostSystem.md "vim.HostSystem"))
-----------------------------------------------------------------
 raises [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost")

---
| service name | CheckAnswerFileStatus |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidProfileReferenceHost](vim.fault.InvalidProfileReferenceHost.md "vim.fault.InvalidProfileReferenceHost") | if the reference host associated with  the profile is incompatible or there is no reference host for the profile. |




QueryAnswerFileStatus([host](vim.HostSystem.md "vim.HostSystem"))
-----------------------------------------------------------------

| service name | QueryAnswerFileStatus |
|:--|:--|
| since version | [vSphere API 5.0](vim.version.md#vim.version.version5) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




