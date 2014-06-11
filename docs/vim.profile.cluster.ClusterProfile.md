vim.profile.cluster.ClusterProfile
==================================
inherits from [vim.profile.Profile](vim.profile.Profile.md "vim.profile.Profile")
as of [vSphere API 4.0](vim.version.md#vim.version.version5)




| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


UpdateClusterProfile([config](vim.profile.cluster.ClusterProfile.ConfigSpec.md "vim.profile.cluster.ClusterProfile.ConfigSpec"))
--------------------------------------------------------------------------------------------------------------------------------
 raises [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName")

---
| service name | UpdateClusterProfile |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version5) |
| privilege    | Profile.Edit |
| return type |  |
### Faults
| fault | description |
|:------|:------------|
| [vim.fault.DuplicateName](vim.fault.DuplicateName.md "vim.fault.DuplicateName") | If the profile with the new name already exists. |




