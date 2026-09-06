```Java
public <T> T calculator(BinaryOperator<T> function, T v1, T v2)
{
  return function.apply(v1, v2);
}

calculator( (var a, var b) -> a + b, 2, 5);
```
