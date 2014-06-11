vim.view.ContainerView
======================
inherits from [vim.view.ManagedObjectView](vim.view.ManagedObjectView.md "vim.view.ManagedObjectView")
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.view.ContainerView.md">ContainerView</a> managed object provides a means of monitoring the contents of   a single container and, optionally, other containers.    You can use a <a href="vim.view.ContainerView.md">ContainerView</a> with a <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> method   to retrieve data or receive notification of changes. For information about using views   with the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>, see the description of <a href="vim.view.ViewManager.md">ViewManager</a>.   <p>   When you invoke the <a href="vim.view.ViewManager.md#createContainerView">CreateContainerView</a> method, you specify   a managed object instance that provides the starting point for object selection.   You can use the following managed objects as the basis of a container view:   <ul>      <li> <a href="vim.Folder.md">Folder</a>      <li> <a href="vim.Datacenter.md">Datacenter</a>      <li> <a href="vim.ComputeResource.md">ComputeResource</a>       <li> <a href="vim.ResourcePool.md">ResourcePool</a>      <li> <a href="vim.HostSystem.md">HostSystem</a>   </ul>   <p>   Once you have created the view, the <a href="vim.view.ManagedObjectView.md#view">view</a> list   always represents the current configuration of the virtual environment and reflects   any subsequent changes that occur.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='container'>container</a> | [vim.ManagedEntity](vim.ManagedEntity.md "vim.ManagedEntity") | None | None | The Folder, Datacenter, ComputeResource, ResourcePool, or HostSystem instance    that provides the objects that the view presents. |
| <a href='type'>type</a> | string | true | None | An optional list of types to be applied to the set of objects in the view.   The list of types indicates objects that are included in the view.    If empty, all types are included. |
| <a href='recursive'>recursive</a> | bool | None | None | Whether to include only the immediate children of the container instance,    or to include additional objects by following the paths beyond the    immediate children.    <p>    For information about recursive behavior, see the description of    <a href="vim.view.ViewManager.md#createContainerView">CreateContainerView</a>. |


