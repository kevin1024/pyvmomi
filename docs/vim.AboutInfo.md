vim.AboutInfo
=============
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


This data object type describes system information   including the name, type, version, and build number.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | Short form of the product name. |
| fullName | string | None | None | The complete product name, including the version information. |
| vendor | string | None | None | Name of the vendor of this product. |
| version | string | None | None | Dot-separated version string. For example, "1.2". |
| build | string | None | None | Build string for the server on which this call is made. For example, x.y.z-num.   This string does not apply to the API. |
| localeVersion | string | true | None | Version of the message catalog for the current session's locale. |
| localeBuild | string | true | None | Build number for the current session's locale.   Typically, this is a small number reflecting a   localization change from the normal product build. |
| osType | string | None | None | Operating system type and architecture.   <p>   Examples of values are:   <ul>   <li>"win32-x86" - For x86-based Windows systems.   <li>"linux-x86" - For x86-based Linux systems.   <li>"vmnix-x86" - For the x86 ESX Server microkernel.   </ul> |
| productLineId | string | None | None | The product ID is a unique identifier for a product line.   <p>   Examples of values are:   <ul>   <li>"gsx" - For the VMware Server product.   <li>"esx" - For the ESX product.   <li>"embeddedEsx" - For the ESXi product.   <li>"vpx" - For the VirtualCenter product.   </ul> |
| apiType | string | None | None | Indicates whether or not the service instance represents a   standalone host.   If the service instance represents a standalone host, then the physical   inventory for that service instance is fixed to that single host.   VirtualCenter server provides additional features over single hosts.   For example, VirtualCenter offers multi-host management.   <p>   Examples of values are:   <ul>   <li>"VirtualCenter" - For a VirtualCenter instance.   <li>"HostAgent" - For host agent on an ESX Server or VMware Server host.   </ul> |
| apiVersion | string | None | None | The version of the API as a dot-separated string. For example, "1.0.0". |
| instanceUuid | string | true | None | A globally unique identifier associated with this service instance. |
| licenseProductName | string | true | None | The license product name |
| licenseProductVersion | string | true | None | The license product version |


