vim.cluster.DasDataSummary
==========================
inherits from [vim.cluster.DasData](docs/vim.cluster.DasData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


This class contains the summary of the data that DAS needs/uses.  The actual data is available in <a href="vim.cluster.DasDataDetails.md">ClusterDasDataDetails</a> and can be retrieved  using the <a href="vim.ClusterComputeResource.md#retrieveDasData">RetrieveDasData</a> method.   This class is meant for VMware internal use only.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| hostListVersion | long | None | None | The version corresponding to the hostList |
| clusterConfigVersion | long | None | None | The version corresponding to the clusterConfig |
| compatListVersion | long | None | None | The version corresponding to the compatList |


