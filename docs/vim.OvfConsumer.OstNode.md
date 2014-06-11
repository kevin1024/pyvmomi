vim.OvfConsumer.OstNode
=======================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)
as of [vSphere API 5.0](vim.version.md#vim.version.version7)


A node in the OVF section tree.   <p>  This class represents a node on which OVF sections can be defined. The possible  node types are OstNodeType.envelope, OstNodeType.virtualSystem or  OstNodeType.virtualSystemCollection, corresponding to the identically named OVF  element types.  <p>  Since the node contains a list of children, it can also be regarded as a tree. This  tree mirrors the structure of the OVF descriptor. It is provided to OVF consumers  as a more convenient way to navigate and modify the OVF than by working directly on  the XML.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| id | string | None | None | The OVF id of the Content (VirtualSystem or VirtualSystemCollection)  element. Empty on the envelope node. |
| type | string | None | None | The type of the node. Possible values are defined in the OstNodeType enum.  <p>  Since the OstNode tree structure mirrors the structure of the OVF descriptor,  only one Envelope node is defined, and it is always the root of the tree. |
| section | [vim.OvfConsumer.OvfSection](vim.OvfConsumer.OvfSection.md "vim.OvfConsumer.OvfSection") | true | None | The list of sections on this node. |
| child | [vim.OvfConsumer.OstNode](vim.OvfConsumer.OstNode.md "vim.OvfConsumer.OstNode") | true | None | The list of child nodes. As dictated by OVF, this list is subject to the  following rules:   <ul>    <li>The Envelope node must have exactly one child.</li>    <li>VirtualSystemCollection nodes may have zero or more children.</li>    <li>VirtualSystem nodes must have no children.</li>  </ul> |
| entity | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | true | None | The VM or vApp corresponding to this node.  <p>  This field is set when this OstNode represents an existing managed entity.   <p>  The entity is unset on nodes of type OstNodeType.envelope. |


