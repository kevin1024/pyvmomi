vim.vApp.VmConfigInfo
=====================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


VM Configuration.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| product | [vim.vApp.ProductInfo](vim.vApp.ProductInfo.md "vim.vApp.ProductInfo") | true | None | Information about the package content. |
| property | [vim.vApp.PropertyInfo](vim.vApp.PropertyInfo.md "vim.vApp.PropertyInfo") | true | None | List of properties |
| ipAssignment | [vim.vApp.IPAssignmentInfo](vim.vApp.IPAssignmentInfo.md "vim.vApp.IPAssignmentInfo") | None | None | IP assignment policy and DHCP support configuration. |
| eula | string | true | None | End User Liceses Agreements. |
| ovfSection | [vim.vApp.OvfSectionInfo](vim.vApp.OvfSectionInfo.md "vim.vApp.OvfSectionInfo") | true | None | List of uninterpreted OVF meta-data sections. |
| ovfEnvironmentTransport | string | true | None | List the transports to use for properties. Supported values are: iso and  com.vmware.guestInfo. |
| installBootRequired | bool | None | None | Specifies whether the VM needs an initial boot before the deployment is complete.  <p>  Not relevant for vApps. This means that the value is always false when reading the  configuration and is ignored when setting the configuration.  <p>  If a vApp requires an install boot (because one of its VMs does), this is visible  on the <a href="vim.VirtualApp.Summary.md#installBootRequired">installBootRequired</a> field of the vApp. |
| installBootStopDelay | int | None | None | Specifies the delay in seconds to wait for the VM to power off after the initial  boot (used only if installBootRequired is true). A value of 0 means wait forever.  <p>  Not relevant for vApps. This means that the value is always false when reading the  configuration and is ignored when setting the configuration. |


