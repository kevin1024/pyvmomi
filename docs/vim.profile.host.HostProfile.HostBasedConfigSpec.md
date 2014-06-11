vim.profile.host.HostProfile.HostBasedConfigSpec
================================================
inherits from [vim.profile.host.HostProfile.ConfigSpec](docs/vim.profile.host.HostProfile.ConfigSpec.md)
as of [vSphere API 4.0](vim.version.md#vim.version.version5)


The <a href="vim.profile.host.HostProfile.HostBasedConfigSpec.md">HostProfileHostBasedConfigSpec</a> data object  specifies the host from which configuration data is to be extracted  and the profile(s) to be created or updated.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| host | [vim.HostSystem](vim.HostSystem.md "vim.HostSystem") | None | None | ESX host. |
| useHostProfileEngine | bool | true | None | Flag indicating if the Profile Engine should use the profile  plug-ins present on the host to create the profile.  If <code>true</code>, the host Profile Engine uses the vSphere 5.0  (or later) profile plug-ins. The resulting profile is not compatible  with legacy hosts (pre 5.0). If <code>false</code> or not specified,  the Profile Engine creates a legacy host profile. |


