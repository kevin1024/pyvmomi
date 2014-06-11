vim.view.View
=============
as of [VI API 2.5](vim.version.md#vim.version.version2)


<a href="vim.view.View.md">View</a> is the base class for session-specific view objects.   A view is a mechanism that supports selection of objects on the server   and subsequently, access to those objects.   To create a view, use the <a href="vim.view.ViewManager.md">ViewManager</a> methods.   A view exists until you terminate it by calling the <a href="vim.view.View.md#destroy">DestroyView</a> method,   or until the end of the session.   Access to a view is limited to the session in which it is created.   <p>   There are three types of views:   <ul>   <li> <a href="vim.view.ContainerView.md">ContainerView</a>   <li> <a href="vim.view.ListView.md">ListView</a>   <li> <a href="vim.view.InventoryView.md">InventoryView</a>   </ul>   <p>   A view maintains a <a href="vim.view.ManagedObjectView.md#view">view</a> list that contains    managed object references. You can use a view    with the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> to retrieve data and   obtain notification of changes to the virtual environment.   For information about using views with the PropertyCollector,    see the description of <a href="vim.view.ViewManager.md">ViewManager</a>.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


DestroyView()
-------------

| service name | DestroyView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | System.View |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




