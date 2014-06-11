vim.CustomizationSpecManager
============================


The CustomizationSpecManager managed object is used to manage  customization specifications stored on the VirtualCenter server.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='info'>info</a> | [vim.CustomizationSpecInfo](vim.CustomizationSpecInfo.md "vim.CustomizationSpecInfo") | true | VirtualMachine.Provisioning.ReadCustSpecs | Gets a list of information on available specifications. |
| <a href='encryptionKey'>encryptionKey</a> | int | true | System.View | Gets a binary public encryption key that can be used to encrypt  passwords in stored specifications. |


DoesCustomizationSpecExist([name](#string "string"))
----------------------------------------------------

| service name | DoesCustomizationSpecExist |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ReadCustSpecs |
| return type | [bool](bool.md "bool") |
### Faults
| fault | description |
|:------|:------------|




GetCustomizationSpec([name](#string "string"))
----------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | GetCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ReadCustSpecs |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |




CreateCustomizationSpec([item](vim.CustomizationSpecItem.md "vim.CustomizationSpecItem"))
-----------------------------------------------------------------------------------------
 raises [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault"), [vim.fault.CannotDecryptPasswords](vim.fault.CannotDecryptPasswords.md "vim.fault.CannotDecryptPasswords"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | CreateCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ModifyCustSpecs |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | vim.fault.CustomizationFault |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | vim.fault.AlreadyExists |
| [vim.fault.CannotDecryptPasswords](vim.fault.CannotDecryptPasswords.md "vim.fault.CannotDecryptPasswords") | vim.fault.CannotDecryptPasswords |




OverwriteCustomizationSpec([item](vim.CustomizationSpecItem.md "vim.CustomizationSpecItem"))
--------------------------------------------------------------------------------------------
 raises [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault"), [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess"), [vim.fault.CannotDecryptPasswords](vim.fault.CannotDecryptPasswords.md "vim.fault.CannotDecryptPasswords"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | OverwriteCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ModifyCustSpecs |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | vim.fault.CustomizationFault |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.ConcurrentAccess](vim.fault.ConcurrentAccess.md "vim.fault.ConcurrentAccess") | vim.fault.ConcurrentAccess |
| [vim.fault.CannotDecryptPasswords](vim.fault.CannotDecryptPasswords.md "vim.fault.CannotDecryptPasswords") | vim.fault.CannotDecryptPasswords |




DeleteCustomizationSpec([name](#string "string"))
-------------------------------------------------
 raises [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DeleteCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ModifyCustSpecs |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |




DuplicateCustomizationSpec([name](#string "string"), [newName](#string "string"))
---------------------------------------------------------------------------------
 raises [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | DuplicateCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ModifyCustSpecs |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | vim.fault.AlreadyExists |




RenameCustomizationSpec([name](#string "string"), [newName](#string "string"))
------------------------------------------------------------------------------
 raises [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RenameCustomizationSpec |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | VirtualMachine.Provisioning.ModifyCustSpecs |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | vim.fault.NotFound |
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | vim.fault.AlreadyExists |




CustomizationSpecItemToXml([item](vim.CustomizationSpecItem.md "vim.CustomizationSpecItem"))
--------------------------------------------------------------------------------------------

| service name | CustomizationSpecItemToXml |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|




XmlToCustomizationSpecItem([specItemXml](#string "string"))
-----------------------------------------------------------
 raises [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault")

---
| service name | XmlToCustomizationSpecItem |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | vim.fault.CustomizationFault |




CheckCustomizationResources([guestOs](#string "string"))
--------------------------------------------------------
 raises [vim.fault.MissingWindowsCustResources](vim.fault.MissingWindowsCustResources.md "vim.fault.MissingWindowsCustResources"), [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault"), [vim.fault.UncustomizableGuest](vim.fault.UncustomizableGuest.md "vim.fault.UncustomizableGuest"), [vim.fault.MissingLinuxCustResources](vim.fault.MissingLinuxCustResources.md "vim.fault.MissingLinuxCustResources")

---
| service name | CheckCustomizationResources |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.CustomizationFault](vim.fault.CustomizationFault.md "vim.fault.CustomizationFault") | vim.fault.CustomizationFault |
| [vim.fault.MissingLinuxCustResources](vim.fault.MissingLinuxCustResources.md "vim.fault.MissingLinuxCustResources") | vim.fault.MissingLinuxCustResources |
| [vim.fault.MissingWindowsCustResources](vim.fault.MissingWindowsCustResources.md "vim.fault.MissingWindowsCustResources") | vim.fault.MissingWindowsCustResources |
| [vim.fault.UncustomizableGuest](vim.fault.UncustomizableGuest.md "vim.fault.UncustomizableGuest") | vim.fault.UncustomizableGuest |




