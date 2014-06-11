vim.cluster.SlotPolicy
======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.1](vim.version.md#vim.version.version8)


The base class <a href="vim.cluster.SlotPolicy.md">ClusterSlotPolicy</a> is used for specifying how  the slot size is to be computed for the failover level HA admission control  policy. By default, vSphere HA defines the slot size using the largest memory  and cpu reservations of any powered on virtual machine in the cluster.  Subclasses of this class define various policies to modify how the slot size  is chosen to prevent outlier virtual machines (i.e. those with much larger  reservations than the average) from skewing the slot size. If such a policy is chosen,  outlier virtual machines will use multiple slots. Using such a policy introduces  a risk that vSphere HA will be unable to failover these virtual machines because  of resource fragmentation.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


