vim.host.NetworkSystem
======================
inherits from [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject")


This managed object type describes networking host configuration and   serves as the top level container for relevant networking   data objects.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='capabilities'>capabilities</a> | [vim.host.NetCapabilities](vim.host.NetCapabilities.md "vim.host.NetCapabilities") | true | None | Capability vector indicating the available product features. |
| <a href='networkInfo'>networkInfo</a> | [vim.host.NetworkInfo](vim.host.NetworkInfo.md "vim.host.NetworkInfo") | true | None | The network configuration and runtime information. |
| <a href='offloadCapabilities'>offloadCapabilities</a> | [vim.host.NetOffloadCapabilities](vim.host.NetOffloadCapabilities.md "vim.host.NetOffloadCapabilities") | true | None | The offload capabilities available on this server. |
| <a href='networkConfig'>networkConfig</a> | [vim.host.NetworkConfig](vim.host.NetworkConfig.md "vim.host.NetworkConfig") | true | None | Network configuration information.  This information can be applied   using the <a href="vim.host.NetworkSystem.md#updateNetworkConfig">updateNetworkConfig()</a> method.  The   information is a strict subset of the information available in NetworkInfo.<br>See <a href="vim.host.NetworkInfo.md">HostNetworkInfo</a><br> |
| <a href='dnsConfig'>dnsConfig</a> | [vim.host.DnsConfig](vim.host.DnsConfig.md "vim.host.DnsConfig") | true | None | Client-side DNS configuration. |
| <a href='ipRouteConfig'>ipRouteConfig</a> | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | The IP route configuration. |
| <a href='consoleIpRouteConfig'>consoleIpRouteConfig</a> | [vim.host.IpRouteConfig](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig") | true | None | IP route configuration for the service console.  The IP route   configuration is global to the entire host.  This property is   set only if   IP routing can be configured for the service console. |


UpdateNetworkConfig([config](vim.host.NetworkConfig.md "vim.host.NetworkConfig"), [changeMode](#string "string"))
-----------------------------------------------------------------------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateNetworkConfig |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | when a network entity specified in the configuration           already exists.<br>See <a href="vim.host.ConfigChange.Mode.md">HostConfigChangeMode</a><br> |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | when a network entity specified in the configuration           already exists.<br>See <a href="vim.host.ConfigChange.Mode.md">HostConfigChangeMode</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.ConfigChange.Mode.md">HostConfigChangeMode</a><br> |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | <br>See <a href="vim.host.ConfigChange.Mode.md">HostConfigChangeMode</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if an invalid parameter is passed in for one           of the networking objects.<br>See <a href="vim.host.ConfigChange.Mode.md">HostConfigChangeMode</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if modify mode is not used, a remove or set           operation is specified for an instance, or a singleton entity           is configured.<br>See <a href="vim.host.ConfigChange.Mode.md">HostConfigChangeMode</a><br> |




UpdateDnsConfig([config](vim.host.DnsConfig.md "vim.host.DnsConfig"))
---------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostInDomain](vim.fault.HostInDomain.md "vim.fault.HostInDomain"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
### Deprecated
As of vSphere API 5.5, which is moved to   each NetStackInstance. This API only works on the default NetStackInstance.

| service name | UpdateDnsConfig |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | when the DHCP virtual network adapter specified does           not exist. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the IP addresses are invalid, or           for a DHCP DNS, if the DHCP virtual network adapter is not specified           or the virtual network adapter specified is not DHCP enabled. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system. |
| [vim.fault.HostInDomain](vim.fault.HostInDomain.md "vim.fault.HostInDomain") | if an attempt is made to change the host or domain name                        while the host is part of a Windows domain. |




UpdateIpRouteConfig([config](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig"))
---------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of vSphere API 5.5, which is moved to   each NetStackInstance. This API only works on the default NetStackInstance.

| service name | UpdateIpRouteConfig |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the an ipv6 address is specified in an ipv4 only           system |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the IP addresses are invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system. |




UpdateConsoleIpRouteConfig([config](vim.host.IpRouteConfig.md "vim.host.IpRouteConfig"))
----------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | UpdateConsoleIpRouteConfig |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the IP addresses are invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system. |




UpdateIpRouteTableConfig([config](vim.host.IpRouteTableConfig.md "vim.host.IpRouteTableConfig"))
------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
### Deprecated
As of vSphere API 5.5, which is moved to   each NetStackInstance. This API only works on the default NetStackInstance.

| service name | UpdateIpRouteTableConfig |
|:--|:--|
| since version | [vSphere API 4.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if any of the IP addresses are invalid. |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system. |




AddVirtualSwitch([vswitchName](#string "string"), [spec](vim.host.VirtualSwitch.Specification.md "vim.host.VirtualSwitch.Specification"))
-----------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | AddVirtualSwitch |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the virtual switch already exists.<br>See <a href="vim.host.NetworkSystem.md#updateVirtualSwitch">UpdateVirtualSwitch</a><br> |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if the physical network adapter being bridged           is already in use.<br>See <a href="vim.host.NetworkSystem.md#updateVirtualSwitch">UpdateVirtualSwitch</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetworkSystem.md#updateVirtualSwitch">UpdateVirtualSwitch</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if network vswitchName exceeds the maximum allowed           length, or the number of ports specified falls out of valid range,           or the network policy is invalid, or beacon configuration is invalid.<br>See <a href="vim.host.NetworkSystem.md#updateVirtualSwitch">UpdateVirtualSwitch</a><br> |




RemoveVirtualSwitch([vswitchName](#string "string"))
----------------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveVirtualSwitch |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual switch does not exist. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if there are virtual network adapters associated           with the virtual switch. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateVirtualSwitch([vswitchName](#string "string"), [spec](vim.host.VirtualSwitch.Specification.md "vim.host.VirtualSwitch.Specification"))
--------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateVirtualSwitch |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if the physical network adapter being bridged is           already in use.<br>See <a href="vim.host.NetworkPolicy.NicOrderPolicy.md">HostNicOrderPolicy</a><br> |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual switch does not exist.<br>See <a href="vim.host.NetworkPolicy.NicOrderPolicy.md">HostNicOrderPolicy</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetworkPolicy.NicOrderPolicy.md">HostNicOrderPolicy</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the bridge parameter is bad or the network policy           is invalid or does not exist or the number of ports specified falls           out of valid range, or the beacon configuration is invalid.<br>See <a href="vim.host.NetworkPolicy.NicOrderPolicy.md">HostNicOrderPolicy</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if network adapter teaming policy is set but           is not supported.<br>See <a href="vim.host.NetworkPolicy.NicOrderPolicy.md">HostNicOrderPolicy</a><br> |




AddPortGroup([portgrp](vim.host.PortGroup.Specification.md "vim.host.PortGroup.Specification"))
-----------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | AddPortGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the port group already exists. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual switch does not exist. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the PortGroup vlanId is invalid.  Valid vlanIds           range from [0,4095], where 0 means no vlan tagging.  Exception is           also thrown if network policy is invalid. |




RemovePortGroup([pgName](#string "string"))
-------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemovePortGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the port group or virtual switch does not exist. |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if the port group can not be removed because there           are virtual network adapters associated with it. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdatePortGroup([pgName](#string "string"), [portgrp](vim.host.PortGroup.Specification.md "vim.host.PortGroup.Specification"))
------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | UpdatePortGroup |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the update causes the port group to conflict           with an existing port group. |
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the port group or virtual switch does not exist. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the PortGroup vlanId is invalid.  Valid vlanIds           range from [0,4095], where 0 means no vlan tagging.  Exception is           also thrown if network policy is invalid. |




UpdatePhysicalNicLinkSpeed([device](#string "string"), [linkSpeed](vim.host.PhysicalNic.LinkSpeedDuplex.md "vim.host.PhysicalNic.LinkSpeedDuplex"))
---------------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdatePhysicalNicLinkSpeed |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the physical network adapter does not exist.<br>See <a href="vim.host.NetCapabilities.md#canSetPhysicalNicLinkSpeed">canSetPhysicalNicLinkSpeed</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetCapabilities.md#canSetPhysicalNicLinkSpeed">canSetPhysicalNicLinkSpeed</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system.<br>See <a href="vim.host.NetCapabilities.md#canSetPhysicalNicLinkSpeed">canSetPhysicalNicLinkSpeed</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the speed and duplexity is not one of the valid           configurations.<br>See <a href="vim.host.NetCapabilities.md#canSetPhysicalNicLinkSpeed">canSetPhysicalNicLinkSpeed</a><br> |




QueryNetworkHint([device](#string "string"))
--------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | QueryNetworkHint |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | System.Read |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if a specified physical network adapter does not exist.<br>See <a href="vim.host.NetCapabilities.md#supportsNetworkHints">supportsNetworkHints</a><br>See <a href="vim.host.PhysicalNic.md#device">device</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetCapabilities.md#supportsNetworkHints">supportsNetworkHints</a><br>See <a href="vim.host.PhysicalNic.md#device">device</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the speed and duplexity combination is not valid           for the current link driver.<br>See <a href="vim.host.NetCapabilities.md#supportsNetworkHints">supportsNetworkHints</a><br>See <a href="vim.host.PhysicalNic.md#device">device</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system.<br>See <a href="vim.host.NetCapabilities.md#supportsNetworkHints">supportsNetworkHints</a><br>See <a href="vim.host.PhysicalNic.md#device">device</a><br> |




AddVirtualNic([portgroup](#string "string"), [nic](vim.host.VirtualNic.Specification.md "vim.host.VirtualNic.Specification"))
-----------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists")

---
| service name | AddVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.AlreadyExists](vim.fault.AlreadyExists.md "vim.fault.AlreadyExists") | if the portgroup already has a virtual network   adapter. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the an ipv6 address is specified in an ipv4 only           system |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the IP address or subnet mask in the IP           configuration are invalid.  In the case of an ESX Server system, DHCP is           not supported and this exception will be thrown if DHCP is           specified.  Exception may also be thrown if the named PortGroup           does not exist. |




RemoveVirtualNic([device](#string "string"))
--------------------------------------------
 raises [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual network adapter cannot be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |




UpdateVirtualNic([device](#string "string"), [nic](vim.host.VirtualNic.Specification.md "vim.host.VirtualNic.Specification"))
-----------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual network adapter cannot be found. |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures. |
| [vim.fault.InvalidState](vim.fault.InvalidState.md "vim.fault.InvalidState") | if the an ipv6 address is specified in an ipv4 only           system |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the IP address or subnet mask in the IP           configuration are invalid.  In the case of an ESX Server           system, DHCP is           not supported and this exception is thrown if DHCP is           specified.  Exception may also be thrown if the named PortGroup           does not exist. |




AddServiceConsoleVirtualNic([portgroup](#string "string"), [nic](vim.host.VirtualNic.Specification.md "vim.host.VirtualNic.Specification"))
-------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported")

---
| service name | AddServiceConsoleVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type | [string](string.md "string") |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the IP address or subnet mask in the IP           configuration are invalid or the named PortGroup does not exist.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |




RemoveServiceConsoleVirtualNic([device](#string "string"))
----------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RemoveServiceConsoleVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual network adapter cannot be found.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if the network adapter is currently used           by DHCP DNS.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |




UpdateServiceConsoleVirtualNic([device](#string "string"), [nic](vim.host.VirtualNic.Specification.md "vim.host.VirtualNic.Specification"))
-------------------------------------------------------------------------------------------------------------------------------------------
 raises [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | UpdateServiceConsoleVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | dynamic |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual network adapter cannot be found.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vim.fault.ResourceInUse](vim.fault.ResourceInUse.md "vim.fault.ResourceInUse") | if tries to turn of DHCP while the network           adapter is currently used by DHCP DNS.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vmodl.fault.InvalidArgument](vmodl.fault.InvalidArgument.md "vmodl.fault.InvalidArgument") | if the IP address or subnet mask in the IP           configuration are invalid or the named PortGroup does not exist.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |




RestartServiceConsoleVirtualNic([device](#string "string"))
-----------------------------------------------------------
 raises [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported"), [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault"), [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound")

---
| service name | RestartServiceConsoleVirtualNic |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.NotFound](vim.fault.NotFound.md "vim.fault.NotFound") | if the virtual network adapter cannot be found.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vim.fault.HostConfigFault](vim.fault.HostConfigFault.md "vim.fault.HostConfigFault") | for all other configuration failures.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |
| [vmodl.fault.NotSupported](vmodl.fault.NotSupported.md "vmodl.fault.NotSupported") | if the host is not an ESX Server system.<br>See <a href="vim.host.NetCapabilities.md#usesServiceConsoleNic">usesServiceConsoleNic</a><br> |




RefreshNetworkSystem()
----------------------

| service name | RefreshNetworkSystem |
|:--|:--|
| since version | [1.0](vim.version.md#None) |
| privilege    | Host.Config.Network |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




