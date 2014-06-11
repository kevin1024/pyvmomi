vim.host.Summary.ConfigSummary
==============================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


An overview of the key configuration parameters.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| name | string | None | None | The name of the host. |
| port | int | None | None | The port number. |
| sslThumbprint | string | true | None | The SSL thumbprint of the host, if known. |
| product | [vim.AboutInfo](vim.AboutInfo.md "vim.AboutInfo") | true | None | Information about the software running on the host, if known.   <p>   The current supported hosts are ESX Server 2.0.1 (and later) and VMware Server   2.0.0 (and later). |
| vmotionEnabled | bool | None | None | The flag to indicate whether or not VMotion is enabled on this host. |
| faultToleranceEnabled | bool | None | None | The flag to indicate whether or not Fault Tolerance logging is enabled on this host. |
| featureVersion | [vim.host.FeatureVersionInfo](vim.host.FeatureVersionInfo.md "vim.host.FeatureVersionInfo") | true | None | List of feature-specific version information. Each element refers  to the version information for a specific feature. |
| agentVmDatastore | [vim.Datastore](vim.Datastore.md "vim.Datastore") | true | None | Datastore used to deploy Agent VMs on for this host. |
| agentVmNetwork | [vim.Network](vim.Network.md "vim.Network") | true | None | Management network for Agent VMs. |


