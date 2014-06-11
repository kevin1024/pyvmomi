vim.host.VFlashManager
======================
as of [vSphere API 5.5](vim.version.md#vim.version.version9)


The VFlash Manager object is used to configure vFlash resource    and vFlash cache on the ESX host.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='vFlashConfigInfo'>vFlashConfigInfo</a> | [vim.host.VFlashManager.VFlashConfigInfo](vim.host.VFlashManager.VFlashConfigInfo.md "vim.host.VFlashManager.VFlashConfigInfo") | true | None | Host vFlash configuration information. |


ConfigureVFlashResourceEx([devicePath](#string "string"))
---------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault")

---
| service name | ConfigureVFlashResourceEx |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type | [vim.Task](vim.Task.md "vim.Task") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | if batch operation fails on the host.   Because the returned VFlashResourceConfigurationResult contains the configuration   success or fault for each device, as of vSphere API 5.x, we won't throw fault when   batch operation fails. |




HostConfigureVFlashResource([spec](vim.host.VFlashManager.VFlashResourceConfigSpec.md "vim.host.VFlashManager.VFlashResourceConfigSpec"))
-----------------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse")

---
| service name | HostConfigureVFlashResource |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | If vFlash resource cannot be configured on the host |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | The contained VFFS volume is being used. |




HostRemoveVFlashResource()
--------------------------
 raises [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | HostRemoveVFlashResource |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.Storage |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If vFlash resource is not configured or the contained VFFS volume                     cannot be found on the host. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | If vFlash resource or the contained VFFS volume cannot                            be removed from the host. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | The contained VFFS volume is being used. |




HostConfigVFlashCache([spec](vim.host.VFlashManager.VFlashCacheConfigSpec.md "vim.host.VFlashManager.VFlashCacheConfigSpec"))
-----------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InaccessibleVFlashSource](vim.fault.InaccessibleVFlashSource.md "vim.fault.InaccessibleVFlashSource"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse")

---
| service name | HostConfigVFlashCache |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.AdvancedConfig |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | If the swap cache cannot be configured on the host. |
| [vim.fault.InaccessibleVFlashSource](vim.fault.InaccessibleVFlashSource.md "vim.fault.InaccessibleVFlashSource") | vFlash resource is not accessible. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | The contained VFFS volume is being used. |




HostGetVFlashModuleDefaultConfig([vFlashModule](#string "string"))
------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | HostGetVFlashModuleDefaultConfig |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version9) |
| privilege    | Host.Config.AdvancedConfig |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | If vFlash resource is not configured or the contained VFFS volume                     cannot be found on the host. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | If the default vFlash module configuration option cannot be                            retrieved. |




