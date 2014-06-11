vmodl.DynamicArray
==================


DynamicArray is a data object type that represents an array of dynamically-typed  objects. A client should only see a DynamicArray object when the element type  is unknown (meaning the type is newer than the client). Otherwise, a client would  see the type as T[] where T is known.

| property | type | optional | priv | desc |
|:---------|:-----|:---------|:-----|:-----|
| dynamicType | string | true | None | Reserved. |
| val | object | None | None | Array of dynamic values. |


