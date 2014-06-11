vim.view.ListView
=================
inherits from [vim.view.ManagedObjectView](vim.view.ManagedObjectView.md "vim.view.ManagedObjectView")
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.view.ListView.md">ListView</a> managed object provides access to updates on a specific set of objects.   You can use a <a href="vim.view.ListView.md">ListView</a> with a <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a> method   to retrieve data or receive notification of changes. For information about using views   with the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>, see the description of <a href="vim.view.ViewManager.md">ViewManager</a>.   <p>   When you invoke the <a href="vim.view.ViewManager.md#createListView">CreateListView</a> method, you specify   a list of objects. The <a href="vim.view.ManagedObjectView.md#view">view</a> list   always represents the current configuration of the virtual environment    and reflects any subsequent changes that occur.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


ModifyListView([add](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"), [remove](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"))
-------------------------------------------------------------------------------------------------------------------------------------------------------

| service name | ModifyListView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | None |
| return type | [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject") |
### Faults
| fault | description |
|:------|:------------|




ResetListView([obj](#vim.ExtensibleManagedObject "vim.ExtensibleManagedObject"))
--------------------------------------------------------------------------------

| service name | ResetListView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | None |
| return type | [vim.ExtensibleManagedObject](vim.ExtensibleManagedObject.md "vim.ExtensibleManagedObject") |
### Faults
| fault | description |
|:------|:------------|




ResetListViewFromView([view](vim.view.View.md "vim.view.View"))
---------------------------------------------------------------

| service name | ResetListViewFromView |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




