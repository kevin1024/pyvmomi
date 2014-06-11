vim.view.ViewManager
====================
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.view.ViewManager.md">ViewManager</a> managed object provides methods to create <a href="vim.view.ContainerView.md">ContainerView</a>,   <a href="vim.view.InventoryView.md">InventoryView</a>, and <a href="vim.view.ListView.md">ListView</a> managed objects.   The <a href="vim.view.ViewManager.md">ViewManager</a> also maintains a list of managed object references   to the views that you have created. Use the <a href="vim.view.ViewManager.md#viewList">viewList</a>    property to access the views.   <p>   A <a href="vim.view.View.md">View</a> is a mechanism that supports selection of objects on the server   and subsequently, access to those objects. Views can simplify the task of    retrieving data from the server. When you use a view, you can use a single   invocation of a <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> method    to retrieve data or receive notification of changes instead of multiple invocations    involving multiple filter specifications. A view exists until you destroy it    or until the end of the session.    <p>   The <a href="vim.view.ViewManager.md">ViewManager</a> supports the following views:   <ul>     <li> A <a href="vim.view.ContainerView.md">ContainerView</a> is based on <a href="vim.Folder.md">Folder</a>,           <a href="vim.Datacenter.md">Datacenter</a>, <a href="vim.ComputeResource.md">ComputeResource</a>,           <a href="vim.ResourcePool.md">ResourcePool</a>, or <a href="vim.HostSystem.md">HostSystem</a> managed objects.           Use a container view to monitor the container contents and optionally,          its descendants.     <li> A <a href="vim.view.ListView.md">ListView</a> managed object is based on an arbitrary but          specific set of objects. When you create a list view, you provide          a list of objects to populate the view          (<a href="vim.view.ViewManager.md#createListView">CreateListView</a>),          or you provide an existing view from which the new view is created          (<a href="vim.view.ViewManager.md#createListViewFromView">CreateListViewFromView</a>).     <li> An <a href="vim.view.InventoryView.md">InventoryView</a> managed object is based on the entire inventory.          Use an inventory view as a general mechanism to monitor the inventory          or portions of the inventory.   </ul>    <p>   For example, you might use the following sequence of operations to get the   names of all the virtual machines on a server:   <ol>     <li> Create a <a href="vim.view.ContainerView.md">ContainerView</a> for the root folder in the server inventory.          For the <a href="vim.view.ContainerView.md">ContainerView</a>, use the <a href="vim.view.ContainerView.md#type">type</a> property          to include only virtual machines.     <li> Create a filter specification for the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>.     <ul>         <li> Use the <a href="vim.view.ContainerView.md">ContainerView</a> as the starting object in the           <a href="vmodl.query.PropertyCollector.ObjectSpec.md">ObjectSpec</a> for the filter.         <li> Use the <a href="vmodl.query.PropertyCollector.TraversalSpec.md">TraversalSpec</a>           to select all objects in the view list (all the virtual machines).         <li> Use the <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a>           to retrieve the name property from each virtual machine.     </ul>     <li> Invoke the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>          <a href="vmodl.query.PropertyCollector.md#retrieveContents">RetrieveProperties</a> method.   </ol>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='viewList'>viewList</a> | [vim.view.View](vim.view.View.md "vim.view.View") | true | System.View | An array of view references. Each array entry is a managed object reference   to a view created by this ViewManager. |


CreateInventoryView()
---------------------

| service name | CreateInventoryView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateContainerView([container](vim.ManagedEntity.md "vim.ManagedEntity"), [type](#string "string"))
----------------------------------------------------------------------------------------------------

| service name | CreateContainerView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateListView([obj](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"))
---------------------------------------------------------------------------------

| service name | CreateListView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CreateListViewFromView([view](vim.view.View.md "vim.view.View"))
----------------------------------------------------------------

| service name | CreateListViewFromView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




