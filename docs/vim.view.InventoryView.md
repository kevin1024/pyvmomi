vim.view.InventoryView
======================
inherits from [vim.view.ManagedObjectView](vim.view.ManagedObjectView.md "vim.view.ManagedObjectView")
as of [VI API 2.5](vim.version.md#vim.version.version2)


The <a href="vim.view.InventoryView.md">InventoryView</a> managed object provides a means of browsing the inventory and tracking   changes to open folders. This managed object is particularly useful for UI clients that   display a tree-based navigation panel of the inventory.   <p>   <a href="vim.view.InventoryView.md">InventoryView</a> maintains the <a href="vim.view.ManagedObjectView.md#view">view</a> list   of managed object references to inventory objects. When you create an inventory view    (<a href="vim.view.ViewManager.md#createInventoryView">CreateInventoryView</a>), the server initializes the view's object   list with a single folder - the root folder.   <p>   <a href="vim.view.InventoryView.md">InventoryView</a> provides methods to open and close folders in the inventory. Use these   methods to add and subtract objects from the <a href="vim.view.ManagedObjectView.md#view">view</a> list.   Use the <a href="vim.view.InventoryView.md">InventoryView</a> together with the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>    to manage the data resulting from <a href="vim.view.InventoryView.md#openFolder">OpenInventoryViewFolder</a>    and <a href="vim.view.InventoryView.md#closeFolder">CloseInventoryViewFolder</a> methods. By using the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>,   you have access to the modifications to the view, rather than processing the entire view list.   <p>   For example, you might use the following sequence of operations with    an <a href="vim.view.InventoryView.md">InventoryView</a> and the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>:   <ol>      <li>Create an <a href="vim.view.InventoryView.md">InventoryView</a>.      <li>Create a filter specification for the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>.      <ul>          <li>Use the <a href="vim.view.InventoryView.md">InventoryView</a> as the starting object in the              <a href="vmodl.query.PropertyCollector.ObjectSpec.md">ObjectSpec</a> for the filter.          <li>Use a set of <a href="vmodl.query.PropertyCollector.TraversalSpec.md">TraversalSpec</a>              data objects to identify paths in possible inventory configurations.          <li>Use the <a href="vmodl.query.PropertyCollector.PropertySpec.md">PropertySpec</a>               to identify object properties for retrieval.      </ul>      <li>Use either the <a href="vmodl.query.PropertyCollector.md#checkForUpdates">CheckForUpdates</a> or           <a href="vmodl.query.PropertyCollector.md#waitForUpdates">WaitForUpdates</a> method to obtain           <a href="vim.view.InventoryView.md">InventoryView</a> modifications. Both methods return          an <a href="vmodl.query.PropertyCollector.UpdateSet.md">UpdateSet</a> object that describes           the changes returned by the <a href="vmodl.query.PropertyCollector.md">PropertyCollector</a>.      <li>Call the <a href="vim.view.InventoryView.md#openFolder">OpenInventoryViewFolder</a> or <a href="vim.view.InventoryView.md#closeFolder">method</a>.   </ol>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|


OpenInventoryViewFolder([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
---------------------------------------------------------------------------

| service name | OpenInventoryViewFolder |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




CloseInventoryViewFolder([entity](vim.ManagedEntity.md "vim.ManagedEntity"))
----------------------------------------------------------------------------

| service name | CloseInventoryViewFolder |
|:--|:--|
| since version | [1.0](vim.version.md#vim.version.version2) |
| privilege    | None |
| return type |  |
### Faults
| fault | description |
|:------|:------------|




