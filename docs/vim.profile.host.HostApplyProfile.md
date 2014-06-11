vim.profile.host.HostApplyProfile
=================================
inherits from [vim.profile.ApplyProfile](docs/vim.profile.ApplyProfile.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.HostApplyProfile.md">HostApplyProfile</a> data object provides access to subprofiles  that contain configuration data for different host capabilities.  The Profile Engine will use any configuration data that you supply  to overwrite the host configuration. See the  <a href="vim.profile.host.HostProfile.md#execute">ExecuteHostProfile</a>  and <a href="vim.profile.host.ProfileManager.md#applyHostConfiguration">ApplyHostConfig_Task</a> methods.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| memory | [vim.profile.host.HostMemoryProfile](vim.profile.host.HostMemoryProfile.md "vim.profile.host.HostMemoryProfile") | true | None | Memory configuration for the host.  This may not be valid for all versions of the host. |
| storage | [vim.profile.host.StorageProfile](vim.profile.host.StorageProfile.md "vim.profile.host.StorageProfile") | true | None | Host storage configuration. |
| network | [vim.profile.host.NetworkProfile](vim.profile.host.NetworkProfile.md "vim.profile.host.NetworkProfile") | true | None | Network configuration. |
| datetime | [vim.profile.host.DateTimeProfile](vim.profile.host.DateTimeProfile.md "vim.profile.host.DateTimeProfile") | true | None | Date and time configuration. |
| firewall | [vim.profile.host.FirewallProfile](vim.profile.host.FirewallProfile.md "vim.profile.host.FirewallProfile") | true | None | Firewall configuration. |
| security | [vim.profile.host.SecurityProfile](vim.profile.host.SecurityProfile.md "vim.profile.host.SecurityProfile") | true | None | Security Configuration of the host.  The security subprofile can include data such as administrator passwords. |
| service | [vim.profile.host.ServiceProfile](vim.profile.host.ServiceProfile.md "vim.profile.host.ServiceProfile") | true | None | Host configuration for services.  Use the <a href="vim.profile.host.ServiceProfile.md#key">key</a> property  to access a subprofile in the list. |
| option | [vim.profile.host.OptionProfile](vim.profile.host.OptionProfile.md "vim.profile.host.OptionProfile") | true | None | List of subprofiles representing advanced configuration options.  Use the <a href="vim.profile.host.OptionProfile.md#key">key</a> property to access a subprofile  in the list. |
| userAccount | [vim.profile.host.UserProfile](vim.profile.host.UserProfile.md "vim.profile.host.UserProfile") | true | None | List of subprofiles for user accounts to be configured on the host.  Use the <a href="vim.profile.host.UserProfile.md#key">key</a> property to access a subprofile  in the list. |
| usergroupAccount | [vim.profile.host.UserGroupProfile](vim.profile.host.UserGroupProfile.md "vim.profile.host.UserGroupProfile") | true | None | List of subprofiles for user groups to be configured on the host.  Use the <a href="vim.profile.host.UserGroupProfile.md#key">key</a> property to access a subprofile  in the list. |
| authentication | [vim.profile.host.AuthenticationProfile](vim.profile.host.AuthenticationProfile.md "vim.profile.host.AuthenticationProfile") | true | None | Authentication Configuration. |


