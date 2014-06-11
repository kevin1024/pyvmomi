vim.option.ArrayUpdateSpec
==========================
inherits from [vmodl.DynamicData](docs/vmodl.DynamicData.md)


An ArrayUpdateSpec data object type is a common superclass    for supporting incremental updates to arrays.   <p>   The common code pattern is:   <pre>      class MyTypeSpec extrends ArrayUpdateSpec {            MyTypeInfo info;      }   </pre>   The ArrayUpdateSpec contains the following:   <p>   <ul>   <li><b>operation</b>: the type of operation being performed.   <li><b>removeKey</b>: In the case of a remove operation, the    key value that identifies the array to be removed.   </ul>

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| operation | [vim.option.ArrayUpdateSpec.Operation](vim.option.ArrayUpdateSpec.Operation.md "vim.option.ArrayUpdateSpec.Operation") | None | None | The type of operation being performed on the specified virtual device. |
| removeKey | object | true | None | Key for the element to be removed. Only used if the operation    is "remove". |


