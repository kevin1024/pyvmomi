vim.host.PatchManager
=====================


This managed object is the interface for scanning and patching an ESX   server.    VMware publishes updates through its external website. A patch update is   synonymous with a bulletin. An update may contain many individual patch   binaries, but its installation and uninstallation are atomic.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


CheckHostPatch([metaUrls](#string "string"), [bundleUrls](#string "string"), [spec](vim.host.PatchManager.PatchManagerOperationSpec.md "vim.host.PatchManager.PatchManagerOperationSpec"))
------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | CheckHostPatch |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | if any error occurs during the operation.           More detailed information will be returned within the payload of the           exception as xml string. |




ScanHostPatch([repository](vim.host.PatchManager.Locator.md "vim.host.PatchManager.Locator"), [updateID](#string "string"))
---------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.PatchMetadataInvalid](vim.fault.PatchMetadataInvalid.md "vim.fault.PatchMetadataInvalid"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
### Deprecated
As of VI API 4.0, use <a href="vim.host.PatchManager.md#ScanV2">ScanHostPatchV2_Task</a>.

| service name | ScanHostPatch |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |
| [vim.fault.PatchMetadataInvalid](vim.fault.PatchMetadataInvalid.md "vim.fault.PatchMetadataInvalid") | if query required metadata is invalid--for           example, it is not found in the repository, is corrupted and           so on. Typically a more specific subclass of PatchMetadataInvalid           is thrown. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | if there is any error in the repository access,           metadata download, repository level integrity check, or reading the           metadata. See <a href="vim.fault.PlatformConfigFault.md#text">text</a> for           specific details. |




ScanHostPatchV2([metaUrls](#string "string"), [bundleUrls](#string "string"), [spec](vim.host.PatchManager.PatchManagerOperationSpec.md "vim.host.PatchManager.PatchManagerOperationSpec"))
-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | ScanHostPatchV2 |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | if there is any error in the repository access,           metadata download, repository level integrity check, or reading the           metadata. See <a href="vim.fault.PlatformConfigFault.md#text">text</a> for           specific details. |




StageHostPatch([metaUrls](#string "string"), [bundleUrls](#string "string"), [vibUrls](#string "string"), [spec](vim.host.PatchManager.PatchManagerOperationSpec.md "vim.host.PatchManager.PatchManagerOperationSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | StageHostPatch |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Patch |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | if the operation is canceled. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | if any error occurs during the operation.           More detailed information will be returned within the payload of the           exception as xml string. |




InstallHostPatch([repository](vim.host.PatchManager.Locator.md "vim.host.PatchManager.Locator"), [updateID](#string "string"))
------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PatchNotApplicable](vim.fault.PatchNotApplicable.md "vim.fault.PatchNotApplicable"), [vim.fault.PatchMetadataInvalid](vim.fault.PatchMetadataInvalid.md "vim.fault.PatchMetadataInvalid"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.PatchBinariesNotFound](vim.fault.PatchBinariesNotFound.md "vim.fault.PatchBinariesNotFound"), [vim.fault.RebootRequired](vim.fault.RebootRequired.md "vim.fault.RebootRequired"), [vim.fault.NoDiskSpace](vim.fault.NoDiskSpace.md "vim.fault.NoDiskSpace"), [vim.fault.PatchInstallFailed](vim.fault.PatchInstallFailed.md "vim.fault.PatchInstallFailed")

---
### Deprecated
Method is deprecated, use <a href="vim.host.PatchManager.md#InstallV2">InstallHostPatchV2_Task</a> instead.

| service name | InstallHostPatch |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Patch |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.PatchMetadataInvalid](vim.fault.PatchMetadataInvalid.md "vim.fault.PatchMetadataInvalid") | if the requried metadata is invalid--for           example, it is not found in the repository, is corrupted and so           on. Typically a more specific subclass of PatchMetadataInvalid is           thrown. |
| [vim.fault.PatchBinariesNotFound](vim.fault.PatchBinariesNotFound.md "vim.fault.PatchBinariesNotFound") | if required update related binaries were not           available. |
| [vim.fault.PatchNotApplicable](vim.fault.PatchNotApplicable.md "vim.fault.PatchNotApplicable") | if the patch is not applicable. Typically a           more specific subclass of PatchNotApplicable is thrown to indicate           a specific problem--for example, PatchSuperseded if the patch is           superseded, MissingDependency if required patch or libraries are not           installed, AlreadyInstalled if the patch is already installed. |
| [vim.fault.NoDiskSpace](vim.fault.NoDiskSpace.md "vim.fault.NoDiskSpace") | if the update can not be installed because there is           insufficent disk space for the installation, including temporary           space used for rollback. |
| [vim.fault.PatchInstallFailed](vim.fault.PatchInstallFailed.md "vim.fault.PatchInstallFailed") | if the installation failed,           <a href="vim.fault.PlatformConfigFault.md#text">text</a> has details of the           failure. Automatic rollback might have succeeded or failed. |
| [vim.fault.RebootRequired](vim.fault.RebootRequired.md "vim.fault.RebootRequired") | if the update cannot be installed without           restarting the host. This might occur on account of a prior           update installation which needed to be installed separately           from other updates. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the host is not in maintenance mode but the           patch install requires all virtual machines to be powered off. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |




InstallHostPatchV2([metaUrls](#string "string"), [bundleUrls](#string "string"), [vibUrls](#string "string"), [spec](vim.host.PatchManager.PatchManagerOperationSpec.md "vim.host.PatchManager.PatchManagerOperationSpec"))
---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | InstallHostPatchV2 |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Patch |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | Thrown if the operation is canceled. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | vim.fault.PlatformConfigFault |




UninstallHostPatch([bulletinIds](#string "string"), [spec](vim.host.PatchManager.PatchManagerOperationSpec.md "vim.host.PatchManager.PatchManagerOperationSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress")

---
| service name | UninstallHostPatch |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Patch |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the feature cannot be supported on the platform,           potentially because the hardware configuration does not support it. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | vim.fault.PlatformConfigFault |




QueryHostPatch([spec](vim.host.PatchManager.PatchManagerOperationSpec.md "vim.host.PatchManager.PatchManagerOperationSpec"))
----------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault"), [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled")

---
| service name | QueryHostPatch |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | System.Read |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vmodl.fault.RequestCanceled](vmodl.fault.RequestCanceled.md "vmodl.fault.RequestCanceled") | vmodl.fault.RequestCanceled |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | If the bulletin ID did not exist. |
| [vim.fault.TaskInProgress](vim.fault.TaskInProgress.md "vim.fault.TaskInProgress") | if there is already a patch installation in progress. |
| [vim.fault.PlatformConfigFault](vim.fault.PlatformConfigFault.md "vim.fault.PlatformConfigFault") | vim.fault.PlatformConfigFault |




