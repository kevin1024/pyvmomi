vim.view.ManagedObjectView
==========================
inherits from [vim.view.View](vim.view.View.md "vim.view.View")
as of [VI API 2.5](vim.version.md#vim.version.version2)


<a href="vim.view.ManagedObjectView.md">ManagedObjectView</a> is the base class for view objects that provide access     to a set of <a href="vim.ManagedEntity.md">ManagedEntity</a> objects. <a href="vim.view.ManagedObjectView.md">ManagedObjectView</a> defines   a view list; the list contains references to objects in the view.   To create a view use the <a href="vim.view.ViewManager.md">ViewManager</a> methods.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| <a href='view'>view</a> | vim.ExtensibleManagedObject | true | None | The list of references to objects mapped by this view. |


