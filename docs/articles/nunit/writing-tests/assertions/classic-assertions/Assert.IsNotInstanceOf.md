# Assert.IsNotInstanceOf


**Assert.IsNotInstanceOf** succeeds if the object provided as an actual value is not an instance of the expected type.

```csharp
Assert.IsNotInstanceOf(Type expected, object actual);
Assert.IsNotInstanceOf(Type expected, object actual,
                       string message, params object[] params);
Assert.IsNotInstanceOf<T>(object actual);
Assert.IsNotInstanceOf<T>(object actual,
                          string message, params object[] params);
```

#### See also...
 * [Type Constraints](xref:constraints#type-constraints)
